# Unidade 7 — Colaboração no GitHub

**Objetivo:** Reconhecer os conceitos de Issues, Pull Requests e Fork usados na colaboração em projetos no GitHub, e praticar cada um.

## Os três conceitos

| Conceito | O que é |
|---|---|
| **Issues** | Um quadro de tarefas, bugs e ideias do projeto. Qualquer pessoa pode abrir uma Issue descrevendo um problema ou sugestão |
| **Fork** | Uma cópia completa de um repositório de outra pessoa, feita na **sua própria conta**, para você poder modificar sem afetar o original |
| **Pull Request (PR)** | Um pedido formal para que suas mudanças (de uma branch ou de um fork) sejam incorporadas ao repositório original, com espaço para revisão e comentários antes de aceitar |

## Abrindo uma Issue

1. No repositório de alguém (ou no seu próprio), clique na aba **Issues**
2. Clique em **New issue**
3. Escreva um título curto e, no corpo, descreva o problema ou a sugestão com detalhes (o que você esperava que acontecesse x o que de fato acontece, se for um bug)
4. Clique em **Submit new issue**

## Fluxo típico de contribuição em projeto de terceiros

1. Faça um **fork** do repositório para a sua conta (botão **Fork**, no canto superior direito do repositório)
2. Clone o fork para sua máquina: `git clone https://github.com/seu-usuario/nome-do-fork.git`
3. Crie uma branch para a sua mudança: `git checkout -b minha-correcao`
4. Faça as alterações, `git add .`, `git commit -m "..."` e `git push origin minha-correcao`
5. No GitHub, na página do seu fork, clique em **Compare & pull request**
6. Escreva um título e uma descrição explicando o que a mudança faz, e clique em **Create pull request**

> 💡 Em projetos próprios ou de equipe pequena, geralmente **não é preciso fork**: basta criar uma branch direto no repositório original e abrir o Pull Request de branch para branch.

## 📝 Exercício de fixação

1. Escolha um repositório público simples no GitHub (pode ser um projeto de exemplo de um colega de turma) e abra uma **Issue** nele descrevendo uma sugestão de melhoria — sem necessariamente implementá-la.
2. Se possível, faça um fork desse mesmo repositório, clone-o, crie uma branch, faça uma pequena alteração (por exemplo, corrigir um erro de digitação no README) e abra um Pull Request seguindo o fluxo acima.
