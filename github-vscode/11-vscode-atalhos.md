# Unidade 11 — VS Code: Atalhos e Produtividade

**Objetivo:** Aplicar atalhos de teclado do VS Code para escrever e navegar pelo código com mais velocidade.

## Tabela de atalhos essenciais

| Ação | Windows/Linux | Mac |
|---|---|---|
| Salvar o arquivo | `Ctrl+S` | `Cmd+S` |
| Comentar/descomentar a linha atual | `Ctrl+/` | `Cmd+/` |
| Desfazer | `Ctrl+Z` | `Cmd+Z` |
| Formatar o documento inteiro | `Shift+Alt+F` | `Shift+Option+F` |
| Abrir arquivo rapidamente pelo nome | `Ctrl+P` | `Cmd+P` |
| Paleta de comandos (busca qualquer ação) | `Ctrl+Shift+P` | `Cmd+Shift+P` |
| Seleciona a próxima ocorrência da palavra (multi-cursor) | `Ctrl+D` | `Cmd+D` |
| Cria um cursor extra no ponto clicado | `Alt+Clique` | `Option+Clique` |
| Insere uma nova linha **abaixo**, mesmo com o cursor no meio da linha atual | `Ctrl+Enter` | `Cmd+Enter` |
| Insere uma nova linha **acima**, mesmo com o cursor no meio da linha atual | `Ctrl+Shift+Enter` | `Cmd+Shift+Enter` |
| Move a linha atual para cima/para baixo | `Alt+↑` / `Alt+↓` | `Option+↑` / `Option+↓` |
| Abre/fecha o terminal integrado | `` Ctrl+` `` | `` Ctrl+` `` |

## Quebra de linha sem precisar ir até o final da linha

O atalho comum de "Enter" só funciona bem quando o cursor já está no final da linha — se ele estiver no meio de um trecho, o Enter normal **quebra o texto ali mesmo**, em vez de criar uma linha nova limpa. Para isso, o VS Code tem um atalho dedicado:

- `Ctrl+Enter` (ou `Cmd+Enter` no Mac) — insere uma linha nova **abaixo** da atual, e já posiciona o cursor nela, não importa em que ponto da linha você estava
- `Ctrl+Shift+Enter` (ou `Cmd+Shift+Enter`) — faz o mesmo, mas insere a linha **acima**

Exemplo prático: se o cursor estiver no meio de uma linha de CSS (ex.: entre `color` e `blue;`) e você quiser abrir uma linha nova logo abaixo sem quebrar o que já estava escrito, use `Ctrl+Enter` em vez do Enter comum.

## A Paleta de Comandos — o atalho mais poderoso

Aperte `Ctrl+Shift+P` (ou `Cmd+Shift+P`) e uma caixa de busca aparece no topo da tela. Digite parte do nome de **qualquer** ação do editor — não precisa saber onde ela fica no menu. Exemplo: digite "format" para achar "Format Document", ou "theme" para achar "Preferences: Color Theme".

## Praticando multi-cursor

1. Abra um arquivo CSS com pelo menos duas classes com o mesmo nome repetido em lugares diferentes (ex.: `.card` aparecendo em 3 regras diferentes)
2. Clique duas vezes sobre a palavra `card` para selecioná-la
3. Aperte `Ctrl+D` (ou `Cmd+D`) repetidas vezes — a cada aperto, a próxima ocorrência da palavra é adicionada à seleção
4. Digite um novo nome — **todas** as ocorrências selecionadas mudam ao mesmo tempo

## 📝 Exercício de fixação

1. Em um arquivo CSS com várias classes repetidas, use `Ctrl+D` (ou `Cmd+D`) para selecionar todas as ocorrências de um nome de classe e renomeie todas ao mesmo tempo.
2. Use `Shift+Alt+F` (ou `Shift+Option+F`) para formatar o arquivo inteiro de uma vez.
3. Abra a Paleta de Comandos (`Ctrl+Shift+P`) e busque por "theme" — experimente trocar o tema de cores do editor só para praticar a busca.
