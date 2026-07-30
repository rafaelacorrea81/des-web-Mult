# Unidade 9 — VS Code: Instalação e Primeiros Passos

**Objetivo:** Instalar o VS Code e reconhecer as áreas principais da interface, mesmo sem nenhuma experiência anterior com editores de código.

> Se você já instalou o VS Code seguindo a Unidade 2 da apostila "Primeiros Passos na Web", pode pular direto para a seção "Reconhecendo a interface" abaixo.

## Instalação

1. Acesse **https://code.visualstudio.com**
2. Clique no botão de download detectado para o seu sistema operacional
3. **Windows:** abra o instalador, aceite os termos, marque **"Adicionar ao PATH"** (geralmente já vem marcada) e clique em Instalar
4. **macOS:** extraia o `.zip` baixado e arraste o ícone para a pasta Aplicativos
5. **Linux:** instale o pacote `.deb` ou `.rpm` baixado, conforme sua distribuição

## Reconhecendo a interface

| Área | O que é |
|---|---|
| **Barra lateral (Activity Bar)** | Coluna de ícones à esquerda: Explorer (arquivos), Busca, Source Control (Git), Debug, Extensões |
| **Explorer** | Mostra a árvore de pastas e arquivos do projeto aberto |
| **Área de edição** | Onde o código é escrito, com abas para múltiplos arquivos abertos ao mesmo tempo |
| **Terminal integrado** | Um terminal completo dentro do próprio editor, sem precisar abrir outro programa — atalho `Ctrl+\`` (Windows/Linux) ou `Cmd+\`` (Mac) |

## Sempre abra a pasta, não o arquivo solto

**Arquivo → Abrir Pasta** (nunca **Arquivo → Abrir Arquivo** para começar um projeto). Isso ativa: busca em todos os arquivos do projeto, o painel Source Control funcionando corretamente, e sugestões de caminho de arquivo corretas (por exemplo, ao digitar `src="img/`, o autocomplete sugere os arquivos que realmente existem na pasta `img`).

## Testando o terminal integrado

1. Abra qualquer pasta de projeto
2. Aperte `` Ctrl+` `` para abrir o terminal
3. Digite `git --version` e aperte Enter
4. **Como saber se deu certo:** aparece um número de versão do Git — se aparecer erro de "comando não encontrado", volte à Unidade 2 (Instalando e Configurando o Git)

## 🎥 Vídeo de apoio

- Instalação e configuração do VS Code para iniciantes: https://www.youtube.com/watch?v=aQXVGHLXJew

## 📝 Exercício de fixação

1. Instale o VS Code (se ainda não tiver).
2. Abra uma pasta de projeto qualquer e identifique, na tela, os quatro elementos da tabela acima (Barra lateral, Explorer, Área de edição, Terminal).
3. Abra o terminal integrado com `` Ctrl+` `` e rode `git --version` dentro dele.
