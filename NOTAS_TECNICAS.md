# Notas técnicas, critérios de aceitação e limitações

## Componentes

- **Formato:** XLSX (Office Open XML), sem arquivos macro-enabled.
- **7 planilhas:** INÍCIO, TITULAR, DEPENDENTES, INFORMES, NOTAS, RESUMO e GUIA.
- **Navegação:** `HYPERLINK` para guias internas, com `IFERROR` como fallback de rótulo.
- **Regras de status:** `IF` + `OR` + `AND`, devolvendo `REVISAR` para informações essenciais ausentes e `PENDENTE` para comprovante não disponível.
- **Indicadores:** `SUM`, `COUNTIF`, `COUNTA`.
- **Entradas:** listas suspensas para padronizar escolhas.
- **Gráficos:** série de rendimentos por natureza.

## Layout de captura

| Área | Faixa de linhas | Capacidade inicial |
| --- | --- | --- |
| DEPENDENTES | 9–48 | 40 registros |
| INFORMES | 9–88 | 80 registros |
| NOTAS | 9–88 | 80 registros |

A capacidade não é ilimitada: ao estender áreas de entrada, revisar totalizadores/formatos/validações correspondentes.

## Testes funcionais (massa de dados fictícia, não distribuída)

Foi feita uma verificação de recálculo com 2 fontes de rendimentos e 2 despesas fictícias:

| Critério | Resultado esperado | Resultado observado |
| --- | ---: | ---: |
| Total de rendimentos (52.000 + 4.350 + 1.200) | R$ 57.550,00 | R$ 57.550,00 |
| Imposto retido cadastrado | R$ 3.600,00 | R$ 3.600,00 |
| Despesas cadastradas (850 + 400) | R$ 1.250,00 | R$ 1.250,00 |
| Pendências de comprovantes | 1 | 1 |
| Informes cadastrados | 2 | 2 |
| Notas cadastradas | 2 | 2 |
| Informe completo e comprovante disponível | OK | OK |
| Nota completa e comprovante pendente | PENDENTE | PENDENTE |

Além disso, foi realizada uma varredura dos resultados da pasta de trabalho em branco, sem ocorrências de `#REF!`, `#DIV/0!`, `#VALUE!`, `#NAME?` ou `#N/A` no mecanismo de cálculo utilizado na verificação.

> **Nota de validação:** testes automatizados verificaram as fórmulas e o conteúdo OOXML. Não substituem a verificação manual no Microsoft Excel de destino para links, formatação visual, impressão e compatibilidade de idioma.

## Limitações conhecidas

1. Não faz cálculo de IR devido, imposto a restituir, limites de dedução ou regras fiscais de exercício.
2. Não valida CPF ou CNPJ por dígito verificador nem consulta fontes externas.
3. A marcação de dedutibilidade e elegibilidade de dependentes é responsabilidade do usuário e depende das regras vigentes.
4. Não faz upload nem guarda PDFs de comprovantes dentro da planilha; o campo de arquivo é apenas referencial.
5. Soma os valores de lançamentos, sem eliminar duplicidades automaticamente.
6. A experiência pode variar fora do Excel desktop, especialmente em links internos e elementos de apresentação.

## Segurança e uso público

O XLSX incluído neste repositório é um **modelo vazio**, não possui macros nem credenciais. A imagem de exemplo utiliza valores totalmente simulados. Recomenda-se publicar o repositório sem versões preenchidas ou pastas de documentos fiscais.
