# Unidade 10 — VS Code: Extensões Essenciais

**Objetivo:** Instalar e reconhecer a função das extensões mais úteis para o desenvolvimento web no dia a dia.

## Como instalar qualquer extensão

1. Clique no ícone de quadrados na barra lateral (Extensões), ou use `Ctrl+Shift+X` (Windows/Linux) / `Cmd+Shift+X` (Mac)
2. Digite o nome da extensão na busca
3. Confira o **nome do autor**, exibido em cinza abaixo do nome da extensão (evita instalar cópias não-oficiais com nome parecido)
4. Clique em **Install**

## As seis extensões essenciais

| Extensão | Autor | Função | Por que usar |
|---|---|---|---|
| **Live Server** | Ritwick Dey | Servidor local com reload automático | Visualiza mudanças em tempo real sem recarregar manualmente |
| **Prettier - Code formatter** | Prettier | Formatação automática de código | Mantém o código limpo e padronizado com um atalho |
| **HTML CSS Support** | ecmel | Sugestões de classes CSS no HTML | Agiliza a escrita e reduz erros de digitação |
| **Auto Rename Tag** | Jun Han | Renomeia tags HTML em par automaticamente | Evita inconsistências ao editar elementos HTML |
| **GitLens** | GitKraken | Integração avançada com Git | Mostra histórico de alterações diretamente no editor, linha a linha |
| **ESLint** | Microsoft | Analisa o código JavaScript em busca de erros e más práticas | Aponta problemas antes mesmo de rodar o código |

## Testando o Prettier

1. Instale o Prettier
2. Abra um arquivo `.css` e bagunce a formatação de propósito (tudo em uma linha só, por exemplo)
3. Salve e aperte `Shift+Alt+F` (Windows/Linux) ou `Shift+Option+F` (Mac)
4. **Como saber se deu certo:** o código se reorganiza sozinho, com indentação e quebras de linha padronizadas

## Testando o Auto Rename Tag

1. Instale a extensão
2. Em um arquivo HTML, clique no nome de uma tag de abertura (ex.: o `div` em `<div>`) e altere para outro nome (ex.: `section`)
3. **Como saber se deu certo:** a tag de fechamento correspondente (`</div>`) muda sozinha para `</section>`, sem você precisar editá-la manualmente

## Cuidado com excesso de extensões

Evite instalar extensões demais "só para garantir" — cada uma consome memória e pode deixar o editor mais lento. Se uma extensão não for usada em semanas, considere desinstalá-la (Extensões → clique com botão direito na extensão → Uninstall).

## 📝 Exercício de fixação

1. Instale as seis extensões da tabela acima, conferindo o autor de cada uma antes de clicar em Install.
2. Teste o Prettier formatando um arquivo bagunçado de propósito.
3. Teste o Auto Rename Tag alterando o nome de uma tag HTML aberta e confirmando que o fechamento acompanha.
