# Unidade 13 — VS Code + Git Integrados

**Objetivo:** Utilizar o painel Source Control do VS Code para fazer stage, commit e push sem sair do editor, e conectar sua conta GitHub à interface.

## Conectando sua conta GitHub ao VS Code

1. Clique no ícone de perfil no canto **inferior esquerdo** da janela do VS Code (ou vá em **Arquivo → Preferências → Contas**)
2. Escolha **"Sign in with GitHub"**
3. Uma aba do navegador abre pedindo autorização — clique em **Authorize**
4. Volte ao VS Code: o ícone de perfil agora mostra sua foto/usuário do GitHub

A partir daqui, toda operação de push/pull feita pela interface do VS Code se autentica sozinha, sem pedir usuário/senha depois.

## O painel Source Control

Abra com o ícone de ramificação na barra lateral, ou `Ctrl+Shift+G` (Windows/Linux) / `Cmd+Shift+G` (Mac).

| Elemento | O que mostra |
|---|---|
| Lista de arquivos modificados | Cada arquivo alterado aparece com uma letra: `M` (modified), `A` (added), `D` (deleted) |
| Botão `+` ao lado de cada arquivo | Equivalente a `git add` naquele arquivo específico, sem digitar comando nenhum |
| Caixa de texto no topo do painel | Onde você escreve a mensagem do commit |
| Ícone de check (✓) ou `Ctrl+Enter` | Confirma o commit dos arquivos em stage |

## Publicando um projeto novo direto pela interface

Se você abriu uma pasta que **ainda não é** um repositório Git:

1. Vá no painel Source Control (`Ctrl+Shift+G`)
2. Clique em **"Publish to GitHub"** (o VS Code detecta que a pasta não está versionada e sugere isso)
3. Escolha se o repositório será público ou privado
4. O VS Code cria o repositório no GitHub **e já faz o primeiro push sozinho** — sem precisar digitar `git init`, `git remote add origin` ou `git push` manualmente

## Fluxo do dia a dia pela interface

1. Modifique um arquivo e salve
2. Ele aparece na lista de modificados no painel Source Control
3. Clique no `+` ao lado do arquivo (stage) — ou passe o mouse sobre "Changes" e clique no `+` para dar stage em tudo de uma vez
4. Escreva a mensagem na caixa de texto
5. Aperte `Ctrl+Enter` (ou clique no ✓) para commitar
6. Clique em **"Sync Changes"** (ou nos ícones de seta, no rodapé) para fazer `pull` e `push` juntos

## GitLens — indo além

Com a extensão GitLens instalada (Unidade 10), cada linha de código passa a mostrar, discretamente ao final da linha, quem foi o autor da última alteração e quando ela ocorreu — útil para entender o histórico de um arquivo sem sair do editor nem digitar `git log`.

## Por que aprender o terminal mesmo tendo a interface gráfica

A interface é ótima para o dia a dia, mas os comandos de terminal (Unidades 2 a 6) funcionam em **qualquer** editor e em servidores sem interface gráfica — e entender o que cada comando faz ajuda a entender o que a interface está fazendo por trás dos botões, principalmente quando algo dá errado e a mensagem de erro aparece só no terminal.

## 📝 Exercício de fixação

1. Conecte sua conta GitHub ao VS Code, seguindo os 4 passos da primeira seção.
2. No projeto que você já versionou (Unidades 3 e 5), modifique um arquivo e faça o commit **inteiramente** pelo painel Source Control (sem digitar nenhum comando `git` no terminal).
3. Envie ao GitHub também pela interface, clicando em "Sync Changes" ou no botão de push.
4. Confirme no site do GitHub que o commit feito pela interface aparece no histórico, com a mensagem que você escreveu.
