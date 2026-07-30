# Unidade 4 — Trabalhando com Branches

**Objetivo:** Criar, alternar e mesclar branches para desenvolver funcionalidades sem afetar a versão principal do projeto.

## O que é uma branch

Uma **branch** (ramo) é uma linha paralela de desenvolvimento. A branch `main` (às vezes chamada `master` em projetos antigos) geralmente representa a versão estável do projeto. Ao criar uma nova funcionalidade, é comum abrir uma branch separada, testar tudo por lá, e só depois juntar (merge) as mudanças de volta à `main`.

## Comandos

```
git branch                     # lista as branches existentes (a atual aparece com um *)
git branch nome-da-branch      # cria uma nova branch, sem mudar para ela
git checkout nome-da-branch    # muda para essa branch
git checkout -b nome-da-branch # cria E já muda para a nova branch, em um único comando
git switch nome-da-branch      # forma mais nova de trocar de branch (equivalente ao checkout)
git merge nome-da-branch       # traz as mudanças da branch informada para a branch atual
```

## Praticando, passo a passo

Usando o repositório `teste-git` da Unidade 3:

1. `git branch` — deve mostrar só `* main` (você está na main, único branch existente)
2. `git checkout -b teste-cor` — cria e já muda para a nova branch
3. Altere o `index.html`, adicionando um estilo de cor de fundo (pode ser um `<body style="background-color: lightblue;">`, só para o teste)
4. `git add .` e `git commit -m "Testa cor de fundo"`
5. `git checkout main` — volta para a branch principal; **repare que o arquivo volta ao estado anterior**, sem a cor — a mudança só existe na branch `teste-cor`
6. `git diff main teste-cor` — mostra a diferença exata entre as duas branches

## Juntando as branches (merge)

Se você decidir manter a mudança:

```
git checkout main
git merge teste-cor
```

Isso traz as mudanças da `teste-cor` para dentro da `main`.

## Boa prática

Em projetos com mais de uma pessoa, evite trabalhar direto na `main`. Crie uma branch por funcionalidade (ex.: `feature/menu-responsivo`), trabalhe nela, e só depois una à `main` — isso evita que um trabalho incompleto quebre a versão estável que outras pessoas estão usando.

## 📝 Exercício de fixação

1. No repositório `teste-git`, crie uma branch chamada `teste-cor` e faça a mudança de cor de fundo, conforme os passos acima.
2. Volte para a `main` e confirme, com `git diff main teste-cor`, que as duas branches estão diferentes.
3. Faça o merge da `teste-cor` para a `main` e confirme, abrindo o `index.html`, que a cor de fundo agora aparece também na `main`.
