# Unidade 3 — Comandos Essenciais do Git

**Objetivo:** Utilizar os comandos básicos do Git para acompanhar o estado de um repositório e registrar mudanças, reconhecendo os três estados de um arquivo.

## Criando seu primeiro repositório de teste

1. Crie uma pasta nova, por exemplo `teste-git`, e abra-a no VS Code (Arquivo → Abrir Pasta)
2. Abra o terminal integrado (`Ctrl+\`` ) e digite:
   ```
   git init
   ```
   **Como saber se deu certo:** aparece a mensagem `Initialized empty Git repository in .../teste-git/.git/`

## Os três estados de um arquivo

| Estado | O que significa |
|---|---|
| **Modified** | O arquivo foi alterado, mas ainda não foi preparado para o commit |
| **Staged** | O arquivo foi adicionado com `git add` e está pronto para entrar no próximo commit |
| **Committed** | A mudança foi registrada no histórico do repositório com `git commit` |

## Comandos, na ordem em que você vai usá-los

```
git status                # mostra o que mudou desde o último commit
git add arquivo.html      # prepara um arquivo específico para o commit
git add .                 # prepara todos os arquivos modificados de uma vez
git commit -m "mensagem"  # registra um ponto de salvamento
git log --oneline         # mostra o histórico de commits, resumido
git diff                  # mostra exatamente o que mudou, linha a linha
```

## Praticando o ciclo completo

1. No terminal, dentro de `teste-git`, digite `git status`. Deve aparecer `No commits yet` e `nothing to commit` (a pasta está vazia).
2. Crie um arquivo `index.html` simples (pode ser só `<h1>Teste</h1>`) e salve.
3. Digite `git status` de novo — agora o arquivo aparece listado em vermelho, em **"Untracked files"** (não rastreado ainda).
4. Digite `git add .` e depois `git status` de novo — o arquivo passa para verde, em **"Changes to be committed"** (staged).
5. Digite `git commit -m "Primeiro commit de teste"`.
6. Digite `git status` de novo — deve aparecer **"nothing to commit, working tree clean"**, confirmando que tudo foi salvo.
7. Digite `git log --oneline` — deve aparecer uma linha com um código curto (hash) e a mensagem "Primeiro commit de teste".

## 🎥 Vídeo de apoio

- Git e GitHub, tutorial completo (cobre os mesmos comandos na prática): https://www.youtube.com/watch?v=_hZf1teRFNg

## 📝 Exercício de fixação

1. Repita o ciclo dos 7 passos acima em uma pasta de teste sua.
2. Altere o conteúdo do `index.html` (mude o texto do `<h1>`), salve, e rode `git diff` **antes** de dar `git add` — confirme que aparece, em vermelho, a linha antiga e, em verde, a linha nova.
3. Complete o commit dessa segunda mudança e rode `git log --oneline` de novo, confirmando que agora aparecem **duas** linhas de commit.
