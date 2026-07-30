# Unidade 2 — Instalando e Configurando o Git

**Objetivo:** Instalar o Git no sistema operacional e configurar identidade (nome e e-mail) usada em todo commit, confirmando cada passo pelo terminal.

## Instalação por sistema operacional

**Windows**
1. Acesse **https://git-scm.com/download/win** — o download deve começar automaticamente
2. Abra o instalador baixado
3. Em todas as telas, pode deixar as opções padrão marcadas e clicar em **Next** — a única tela que vale conferir é a de "Adjusting your PATH environment", onde a opção recomendada (geralmente já marcada) é **"Git from the command line and also from 3rd-party software"**
4. Clique em **Install** e, ao final, em **Finish**

**macOS**
- A forma mais simples: abra o **Terminal** e digite `git --version`. Se o Git ainda não estiver instalado, o macOS oferece para instalar as "Command Line Tools" automaticamente — aceite.
- Alternativa, se você já usa Homebrew: `brew install git`

**Linux (Debian/Ubuntu)**
```
sudo apt update
sudo apt install git
```

## Confirmando a instalação

Abra um terminal (no VS Code, `Ctrl+\`` ) e digite:

```
git --version
```

**Como saber se deu certo:** aparece uma linha como `git version 2.4x.x.windows.1` (o número exato varia). Se aparecer uma mensagem de "comando não encontrado", a instalação não terminou corretamente ou o terminal precisa ser reaberto (fechar e abrir de novo o VS Code costuma resolver, no Windows).

## Configurando sua identidade

Todo commit fica assinado com um nome e um e-mail. Configure isso **uma única vez por computador** — vale para todos os projetos:

```
git config --global user.name "Seu Nome"
git config --global user.email "seu-email@exemplo.com"
```

Use o mesmo e-mail que você usa (ou vai usar) na sua conta do GitHub (Unidade 5) — isso faz o GitHub reconhecer seus commits como seus, com sua foto de perfil no histórico.

## Conferindo o que foi salvo

```
git config --list
```

**Como saber se deu certo:** entre as linhas exibidas, devem aparecer `user.name=Seu Nome` e `user.email=seu-email@exemplo.com`, com os valores exatos que você digitou.

> 💡 `--global` aplica a configuração a todos os repositórios do seu usuário no computador. Sem essa flag, a configuração vale só para o repositório da pasta atual — útil quando você usa e-mails diferentes para projetos pessoais e de trabalho.

## 📝 Exercício de fixação

1. Instale o Git seguindo as instruções do seu sistema operacional.
2. Rode `git --version` e confirme que aparece um número de versão.
3. Configure seu nome e e-mail com `--global`.
4. Rode `git config --list` e confirme, na tela, que os dois valores aparecem exatamente como você digitou (sem erros de digitação — isso vai aparecer em todo commit que você fizer daqui para frente).
