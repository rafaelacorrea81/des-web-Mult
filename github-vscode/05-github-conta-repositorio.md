# Unidade 5 — GitHub: Criando Conta e Repositório Remoto

**Objetivo:** Criar uma conta no GitHub, criar um repositório remoto e conectá-lo a um repositório local, do zero.

## Passo 1 — Criar a conta

1. Acesse **https://github.com**
2. Clique em **Sign up**, no canto superior direito
3. Preencha e-mail, crie uma senha e escolha um nome de usuário (esse nome aparece na URL dos seus projetos publicados — evite espaços e caracteres especiais)
4. Resolva a verificação de segurança (um quebra-cabeça visual simples) e clique em **Create account**
5. O GitHub envia um código de verificação para seu e-mail — digite-o na tela seguinte para confirmar a conta

## Passo 2 — Criar um repositório novo

1. Já logado, clique no ícone **+** no canto superior direito → **New repository**
2. Em **Repository name**, digite um nome (ex.: `meu-primeiro-site`)
3. Deixe **Public** selecionado (necessário para usar o GitHub Pages gratuito depois)
4. **Não marque** a caixa **"Add a README file"** se você já tem um projeto local pronto — isso evita um conflito de histórico no primeiro envio
5. Clique em **Create repository**
6. Na página seguinte, copie a URL mostrada (formato `https://github.com/seu-usuario/meu-primeiro-site.git`)

## Passo 3 — Conectando o repositório local ao remoto

No terminal, dentro da pasta do seu projeto (que já deve ter passado por `git init`, `git add`, `git commit` — Unidade 3):

```
git remote add origin https://github.com/seu-usuario/meu-primeiro-site.git
git branch -M main
git push -u origin main
```

Troque a URL pela que você copiou no Passo 2.

**Como saber se deu certo:** recarregue a página do repositório no GitHub (F5) — os arquivos do projeto devem aparecer listados.

## Trazendo mudanças do remoto (em outro computador, por exemplo)

```
git clone https://github.com/seu-usuario/meu-primeiro-site.git   # copia um repositório existente para uma pasta nova
git pull                                                          # baixa e mescla mudanças novas do remoto
```

## O que significa "origin" e o "-u"

`origin` é apenas um apelido (você poderia escolher outro nome) para a URL do repositório remoto. O `-u` em `git push -u origin main`, usado só na primeira vez, cria a ligação entre a branch local `main` e a branch remota `main` — depois disso, basta digitar `git push` sozinho, sem repetir `origin main`.

## Se pedir autenticação

Na primeira vez que você fizer `git push`, pode abrir uma janela do navegador pedindo para autorizar o acesso à sua conta GitHub — clique em **Authorize**. Se em vez disso aparecer um campo de senha direto no terminal, veja a nota sobre autenticação na Unidade 13 (VS Code + Git Integrados).

## 🎥 Vídeo de apoio

- GitHub, guia completo para iniciantes: https://www.youtube.com/watch?v=BUGZZaChiYw

## 📝 Exercício de fixação

1. Crie sua conta no GitHub (se ainda não tiver) seguindo o Passo 1.
2. Crie um repositório novo (Passo 2) para um projeto seu.
3. Conecte-o ao repositório local (Passo 3) e confirme, no site, que os arquivos e o histórico de commits aparecem corretamente.
