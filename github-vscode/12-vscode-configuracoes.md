# Unidade 12 — VS Code: Configurações e Personalização

**Objetivo:** Ajustar tema, fonte e comportamento do editor por meio das configurações visuais e do arquivo `settings.json`.

## Pela tela de configurações (mais fácil para começar)

- **Tema de cores:** menu **Arquivo → Preferências → Tema de Cores** (ou `Ctrl+K Ctrl+T`). Um tema escuro costuma reduzir o cansaço visual em sessões longas.
- **Configurações gerais:** `Ctrl+,` (vírgula) abre a tela de Configurações, com busca por palavra-chave (tamanho de fonte, tabulação, quebra de linha, etc.) — digite o que procura na caixa de busca no topo.

## Pelo `settings.json` (configuração em texto)

Toda opção alterada na tela de Configurações também pode ser escrita diretamente em texto. Para abrir:

1. `Ctrl+Shift+P` (ou `Cmd+Shift+P`)
2. Digite **"Preferences: Open User Settings (JSON)"** e aperte Enter
3. Adicione (ou edite) as linhas:

```json
{
  "editor.fontSize": 15,
  "editor.formatOnSave": true,
  "editor.tabSize": 2,
  "files.autoSave": "onFocusChange",
  "workbench.colorTheme": "Default Dark+"
}
```

- `editor.fontSize` — tamanho da fonte no editor
- `editor.formatOnSave` — formata o código automaticamente toda vez que você salva (combine com o Prettier da Unidade 10 para eliminar a necessidade do atalho manual)
- `editor.tabSize` — quantos espaços cada tabulação representa
- `files.autoSave` — salva sozinho quando você troca de aba ou de janela
- `workbench.colorTheme` — nome exato do tema escolhido (deve bater com o nome mostrado na lista de temas)

## Confirmando que funcionou

1. Salve o `settings.json` (`Ctrl+S`)
2. Abra um arquivo `.css` bagunçado (sem formatação) que você tenha o Prettier instalado
3. Salve esse arquivo (`Ctrl+S`) — com `editor.formatOnSave: true`, ele deve se formatar **sozinho**, sem precisar do atalho `Shift+Alt+F`

## 📝 Exercício de fixação

1. Abra seu `settings.json` e adicione as cinco configurações do exemplo acima, ajustando os valores ao seu gosto (por exemplo, um `fontSize` diferente).
2. Teste a `editor.formatOnSave` conforme o passo "Confirmando que funcionou" acima.
3. Troque o `workbench.colorTheme` para outro tema instalado e confirme que a cor do editor muda ao salvar.
