# Unidade 6 — .gitignore e Boas Práticas de Commit

**Objetivo:** Configurar um arquivo `.gitignore` e escrever mensagens de commit claras e úteis.

## Por que ignorar arquivos

Nem tudo que existe na pasta do projeto deveria ir para o repositório: pastas geradas automaticamente (como `node_modules`, em projetos com Node.js), arquivos de configuração pessoal do editor, ou arquivos temporários. O arquivo `.gitignore` lista o que o Git deve **ignorar** e nunca enviar ao repositório.

## Criando o arquivo

Na raiz do seu projeto (mesmo nível do `index.html`), crie um arquivo chamado exatamente `.gitignore` (com o ponto no início, sem extensão) e adicione:

```
node_modules/
.DS_Store
*.log
.vscode/
.env
```

- `node_modules/` — pasta pesada, gerada automaticamente por gerenciadores de pacotes (não usada nesta apostila, mas comum em projetos maiores)
- `.DS_Store` — arquivo criado automaticamente pelo macOS em cada pasta
- `*.log` — qualquer arquivo terminado em `.log`
- `.vscode/` — configurações específicas do seu VS Code local
- `.env` — arquivo onde normalmente ficam senhas e chaves de configuração

> ⚠️ **Nunca versione arquivos com senhas, chaves de API ou dados sensíveis** (geralmente guardados em `.env`). Uma vez enviados ao GitHub, esses dados ficam no histórico mesmo que o arquivo seja apagado depois — é preciso reescrever o histórico do zero para removê-los de verdade.

## Confirmando que o `.gitignore` está funcionando

1. Crie uma pasta vazia chamada `node_modules` dentro do seu projeto, só para o teste
2. Rode `git status`
3. **Como saber se deu certo:** essa pasta **não** deve aparecer na lista de arquivos não rastreados — o Git já a ignora, por causa da regra no `.gitignore`

## Boas práticas de mensagem de commit

- Escreva no **imperativo**: "Corrige alinhamento do menu", não "Corrigido" ou "Correções"
- **Uma mudança lógica por commit** — evite misturar "ajusta CSS" com "adiciona nova página" no mesmo commit
- Mensagens curtas na primeira linha (até ~50 caracteres); detalhes extras podem ir em uma segunda linha, separada por uma linha em branco

## 📝 Exercício de fixação

1. Crie um `.gitignore` no seu projeto com as cinco linhas do exemplo acima.
2. Crie uma pasta `node_modules` vazia (só para teste) e confirme, com `git status`, que ela não aparece como pendente para commit.
3. Reescreva estas três mensagens de commit ruins, seguindo as boas práticas acima: "coisas", "correção", "att".
