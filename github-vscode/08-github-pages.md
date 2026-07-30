# Unidade 8 — Publicando com GitHub Pages

**Objetivo:** Publicar um site estático gratuitamente utilizando o GitHub Pages, passo a passo, sem travar.

## Pré-requisito

Você já precisa ter um repositório no GitHub com os arquivos do seu site (Unidade 5).

## Passo a passo

1. Abra o repositório do seu site em **github.com**
2. No menu superior do repositório, clique em **Settings**
3. No menu lateral esquerdo, clique em **Pages**
4. Em **"Build and deployment"**, no campo **Source**, escolha a fonte:
   - **Deploy from a branch** — mais simples, recomendado para este material
   - **GitHub Actions** — para projetos com processo de build (React, Vue, etc.), fora do escopo aqui
5. Com **"Deploy from a branch"** selecionado, escolha a branch **main** e a pasta **`/ (root)`**
6. Clique em **Save**
7. Aguarde 1 a 3 minutos e recarregue a página (F5) — uma faixa verde aparece no topo com o link do site:
   ```
   https://seu-usuario.github.io/nome-do-repositorio/
   ```

## Se o link der erro 404

Aguarde mais 1 a 2 minutos (o GitHub ainda está processando a primeira publicação) e recarregue. Se persistir depois de 5 minutos, confirme que a branch selecionada no passo 5 é a mesma onde estão os arquivos (`main`) e que existe um `index.html` na raiz do repositório.

## O caso especial do domínio raiz

Se o repositório se chamar **exatamente** `seu-usuario.github.io`, o site fica disponível direto na raiz (`https://seu-usuario.github.io/`), sem o caminho extra do nome do repositório.

## Cuidado com links internos

> ⚠️ Links que começam com `/` (barra) podem quebrar no GitHub Pages, porque o site não fica na raiz do domínio, e sim em um subcaminho (`/nome-do-repositorio/`). Prefira caminhos **relativos**, como `./css/estilos.css` ou `css/estilos.css` (sem barra no início).

## Atualizando o site depois de publicado

Basta repetir o fluxo do dia a dia do Git: `git add .` → `git commit -m "..."` → `git push`. O GitHub Pages atualiza sozinho, alguns minutos depois de cada push na branch configurada — não é preciso repetir a configuração de Settings → Pages.

## 🎥 Vídeo de apoio

- Publicando um site com GitHub Pages: https://www.youtube.com/watch?v=9iZ-xRiF62Q

## 📝 Exercício de fixação

1. Publique um projeto seu com o GitHub Pages, seguindo os 7 passos acima.
2. Acesse o link final em uma **aba anônima** do navegador, para confirmar que o site está realmente público (não aparecendo só porque você está logado).
3. Altere algo no `index.html`, faça o fluxo `git add` → `git commit` → `git push`, aguarde 2 minutos e recarregue o link público para confirmar que a mudança chegou até lá.
