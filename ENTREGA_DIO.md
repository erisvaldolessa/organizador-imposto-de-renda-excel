# Publicação no GitHub e entrega do desafio DIO

Este pacote já contém a planilha, documentação, capturas de tela e arquivo de exclusão. **Não é necessário escrever nenhum código.**

## Dados do repositório — copiar e colar

**Nome do repositório:**

```text
organizador-imposto-de-renda-excel
```

**Descrição curta para o GitHub:**

```text
Organizador de Imposto de Renda em Excel com cadastro, informes, comprovantes, navegação, validações e painel-resumo. Projeto DIO.
```

**Tópicos sugeridos:**

```text
excel  dio  imposto-de-renda  planilhas  organizacao-financeira  portfolio
```

**Visibilidade:** Público (para a avaliação na plataforma).

## Opção A — Publicar pelo navegador (mais simples)

1. Acesse https://github.com/ e entre na sua conta.
2. Clique em **+** > **New repository** (ou acesse https://github.com/new).
3. Digite o nome e a descrição sugeridos acima; selecione **Public**.
4. Clique em **Create repository**. Para evitar conflitos de arquivos, não peça para gerar README ou `.gitignore` automaticamente: eles já estão incluídos neste pacote.
5. Selecione **uploading an existing file** (ou **Add file** > **Upload files**).
6. **Extraia o ZIP** recebido. Envie o conteúdo **de dentro da pasta** `organizador-imposto-de-renda-excel`, mantendo `docs/` e `images/` e os arquivos no nível principal. *Não envie apenas o ZIP como um único arquivo*.
7. Descreva o commit como `feat: publica organizador de imposto de renda em Excel`.
8. Clique em **Commit changes**. O GitHub deve exibir o `README.md` automaticamente.
9. Confirme que o arquivo XLSX abre/baixa e que as duas imagens aparecem no README.
10. Copie o endereço do repositório: `https://github.com/SEU-USUARIO/organizador-imposto-de-renda-excel` (substitua `SEU-USUARIO` pelo usuário real).

> Dica: se o navegador não preservar a estrutura de pastas, envie primeiro os arquivos da raiz; depois use **Add file > Upload files** para `docs/` e `images/`, arrastando os arquivos conforme a interface disponível.

## Opção B — Publicar pelo Git (terminal)

Esta alternativa pressupõe Git instalado e autenticação no GitHub. Primeiro crie um repositório **público vazio** no GitHub. Depois, abra o terminal na pasta extraída e rode:

```bash
git init
git add README.md Organizador_Imposto_de_Renda_DIO.xlsx ENTREGA_DIO.md .gitignore docs images
git commit -m "feat: publica organizador de imposto de renda em Excel"
git branch -M main
git remote add origin https://github.com/SEU-USUARIO/organizador-imposto-de-renda-excel.git
git push -u origin main
```

Substitua `SEU-USUARIO` pelo seu nome de usuário. Não digite senha do GitHub em arquivos do repositório.

## Entrega na plataforma DIO

Depois que a página pública do repositório estiver no ar, volte à aula **Entendendo o Desafio** > **Entregar Projeto**.

**Link para enviar:** a URL real do repositório público (não o caminho local nem a URL de um arquivo ZIP).

**Título sugerido:**

```text
Organizador de Declaração de Imposto de Renda em Excel
```

**Descrição para colar:**

```text
Desenvolvi um organizador de informações para a declaração de Imposto de Renda em Excel. A solução reúne cadastro do titular e dependentes, registro de informes de rendimentos, organização de notas e comprovantes, listas de validação, indicadores de conferência e painel-resumo com consolidação automática. O projeto inclui documentação, guia de utilização, imagens demonstrativas e testes com dados fictícios. O modelo público é disponibilizado sem informações pessoais reais e não substitui os sistemas oficiais da Receita Federal.
```

## Conferência antes de enviar

- [ ] O repositório está público.
- [ ] O `README.md` aparece formatado na página inicial.
- [ ] O XLSX está acessível e contém as 7 abas.
- [ ] As imagens do início e do resumo aparecem.
- [ ] Os guias técnicos em `docs/` estão acessíveis.
- [ ] Não existem dados pessoais, recibos, declarações ou documentos privados no repositório.
- [ ] O link colado na DIO é o do repositório real.

**Importante:** O nome e o endereço do repositório acima são sugestões. O link real só existirá depois da publicação na sua conta.
