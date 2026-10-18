# Organizador de Declaração de Imposto de Renda | Excel

**Projeto do desafio prático da DIO — Criando um Organizador de Declaração de Imposto de Renda**

Uma ferramenta em Excel para **centralizar dados cadastrais, informes de rendimentos, despesas e comprovantes** utilizados na preparação documental para a declaração de Imposto de Renda. Inclui navegação interna, menus suspensos, alertas de preenchimento e resumo automático dos registros.

> **Escopo educacional:** o arquivo é um *organizador de informações*, não um programa de cálculo ou transmissão da declaração. Totais, indicadores e status não validam documentação nem determinam elegibilidade a deduções fiscais. Consulte as regras vigentes e os canais oficiais da Receita Federal.

## Prévia da solução

**Página inicial — navegação entre abas**

![Tela inicial do organizador de IR](images/visao_geral.png)

**Painel de acompanhamento — exemplo com dados fictícios**

![Painel-resumo ilustrativo com valores fictícios](images/painel_resumo_exemplo.png)

> As imagens ilustram o funcionamento. A **planilha distribuída está vazia**, sem CPF, endereço, renda ou qualquer informação pessoal real. A segunda imagem foi produzida a partir de um cenário simulado e não corresponde a dados presentes no arquivo público.

## Como acessar

1. Baixe o arquivo [`Organizador_Imposto_de_Renda_DIO.xlsx`](Organizador_Imposto_de_Renda_DIO.xlsx).
2. Abra no **Microsoft Excel** (preferencialmente na versão para computador) e habilite o cálculo automático, caso esteja desativado.
3. Use os atalhos da aba **INÍCIO** para acessar os formulários, ou navegue pelas guias inferiores.
4. Preencha exclusivamente as áreas editáveis, sinalizadas em azul-claro, em uma **cópia privada** para uso com informações reais.
5. Consulte **RESUMO** para acompanhar totais e pendências.

Não é necessário habilitar macros, instalar extensões ou criar contas externas para usar a planilha.

## Estrutura da pasta de trabalho

| Aba | Finalidade | Recursos principais |
| --- | --- | --- |
| **INÍCIO** | Menu de navegação e visão rápida. | Links internos, contadores e alertas. |
| **TITULAR** | Cadastro dos dados essenciais. | Formulário, listas suspensas e verificação de campos obrigatórios. |
| **DEPENDENTES** | Organização de pessoas vinculadas. | Relação familiar, vínculo e comprovantes. |
| **INFORMES** | Registro de fontes pagadoras e rendimentos. | Categorias, IRRF, previdência e status automático de conferência. |
| **NOTAS** | Registro de despesas e documentos. | Categorias, valor, indicação manual de dedutibilidade e pendências. |
| **RESUMO** | Consolidação gerencial. | Indicadores financeiros, contagens e gráfico. |
| **GUIA** | Orientações dentro do próprio Excel. | Passo a passo de preenchimento e alerta de privacidade. |

## Funcionalidades e fórmulas

- **Navegação interna:** links pelas células da aba INÍCIO e retorno ao menu.
- **Validação por listas:** tipos de declaração, unidades federativas, relações, tipos de rendimentos, categorias de despesas e disponibilidade do comprovante.
- **Conferência:** estados `OK`, `REVISAR` e `PENDENTE`, calculados com `SE` (`IF`), `E` (`AND`) e `OU` (`OR`) conforme a configuração de idioma do Excel.
- **Consolidação:** `SOMA` (`SUM`), `CONT.SE` (`COUNTIF`) e `CONT.VALORES` (`COUNTA`) para totais e contagens.
- **Painel:** separação entre rendimentos tributáveis, isentos e sujeitos à tributação exclusiva; IR retido, despesas cadastradas e pendências.
- **Privacidade:** estrutura inicial em branco e **sem macros (VBA)** e sem conexões externas.

As áreas de lançamentos são predefinidas: **40 linhas** para dependentes e **80 linhas** em cada uma das abas INFORMES e NOTAS. Caso precise exceder esses limites, é necessário ampliar também as fórmulas e o resumo.

## Regras de interpretação

- `OK` significa apenas que os **campos de conferência esperados para aquela linha** foram preenchidos, não que o registro seja fiscalmente válido.
- `REVISAR` indica informação essencial não informada na linha cadastrada.
- `PENDENTE` indica comprovante classificado como pendente.
- O campo **Dedutibilidade** é preenchido pelo usuário: **não é uma análise de enquadramento fiscal**.
- O CPF é tratado como texto para preservar zeros; o arquivo **não valida os dígitos verificadores**.
- Os valores do resumo são somas simples dos registros. Não representam base de cálculo do IR, imposto devido ou restituição.

## Documentação

- [Guia de preenchimento e boas práticas](docs/GUIA_DE_USO.md)
- [Arquitetura funcional, testes e limitações](docs/NOTAS_TECNICAS.md)
- [Roteiro pronto para publicar no GitHub e entregar na DIO](ENTREGA_DIO.md)

## Tecnologias e compatibilidade

- Microsoft Excel / `.xlsx` (sem VBA).
- Fórmulas, formatação condicional, validação de dados e gráfico incorporado.
- Desenvolvido com apoio de ferramenta de inteligência artificial e revisão por testes em cenário fictício; verifique o comportamento no Excel da sua instalação.
- Editores alternativos podem apresentar diferenças em links internos, formatação e validação de dados.

## Privacidade e segurança

**Nunca publique uma cópia preenchida com dados reais em repositórios públicos.** Para uso pessoal, faça download do modelo e salve uma cópia em local privado. Não adicione declarações, PDFs, informes, recibos, certificados ou senhas ao repositório.

Este projeto demonstra técnicas de organização documental e automação de planilhas. Não há associação, homologação ou endosso da Receita Federal.

## Autor e contexto

Projeto de portfólio educacional desenvolvido para a trilha de Excel com IA da **DIO**, com auxílio de ferramentas de IA na organização e documentação técnica.
