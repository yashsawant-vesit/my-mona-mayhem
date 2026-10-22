<!-- l10n-sync: source-file="workshop/03-agent-mode.md" -->
# Parte 3: Construa o jogo com fluxos de trabalho agênticos

---

Nesta parte, o Copilot passa de planejador a implementador. Em vez de escrever código linha por linha, descreva o que você quer e deixe o Copilot trabalhar nos arquivos que precisar alterar.

## Tarefa 1: Conecte a batalha

<!-- track:vscode:start -->
1. Mude para o modo **Agent** no Copilot Chat.
2. Digite este prompt:
<!-- track:vscode:end -->

<!-- track:cli:start -->
1. Volte ao fluxo padrão de programação do Copilot CLI (ou continue no autopilot se quiser que o Copilot siga trabalhando até você pará-lo).
2. Se for útil, adicione contexto indicando o arquivo da página: `@src/pages/index.astro`.
3. Digite este prompt:
<!-- track:cli:end -->

   > Adicione JavaScript no cliente à página de batalha que:
   > 1. Ao clicar no botão Battle, obtenha os dois nomes de usuário dos campos.
   > 2. Verifique se ambos foram preenchidos (e mostre um erro caso contrário).
   > 3. Busque os dados de contribuição dos dois usuários em paralelo pela nossa API.
   > 4. Exiba os gráficos de contribuição como grades coloridas — cada dia é um quadrado colorido que usa a paleta do GitHub.
   > 5. Mostre um selo VS entre os dois usuários.
   > 6. Exiba o nome de usuário, o total de contribuições e o intervalo de datas de cada pessoa.
   > 7. Trate os estados de carregamento e os erros.
   > 8. Também inicie a batalha ao pressionar Enter nos campos.
   > 9. Use a interface simples que já está pronta.
   >
   > Use interfaces TypeScript para a estrutura dos dados de contribuição.

<!-- track:vscode:start -->
3. Deixe o Agent Mode implementar as alterações em `index.astro`.
4. Revise as alterações propostas na visualização de diff antes de aceitá-las.
<!-- track:vscode:end -->

<!-- track:cli:start -->
4. Deixe o Copilot CLI implementar as alterações em `src/pages/index.astro`.
5. Inspecione as alterações geradas com `/diff` e aprove-as.
<!-- track:cli:end -->

## Tarefa 2: Teste a batalha

> **⚠️ Não está vendo as alterações?** Se a página de batalha não tiver sido atualizada, pare o servidor de desenvolvimento (`Ctrl+C`), reinicie com `npm run dev` e atualize o navegador.

1. Digite `octocat` e `torvalds` nos campos de nome de usuário e clique em **Battle**.
2. Você deve ver os gráficos de contribuição dos dois usuários lado a lado, com grades coloridas.
3. Teste os casos de erro:
   - Deixe um ou os dois campos vazios e clique em Battle — deve aparecer um erro de validação.
   - Digite um nome de usuário inválido — o aplicativo deve exibir um erro da API.
4. Pressione **Enter** em qualquer campo; isso deve iniciar a batalha como o clique no botão.

## Tarefa 3: Itere com o Copilot

Se algo não estiver totalmente certo, envie feedback diretamente ao Copilot. Por exemplo:

- *“Os quadrados de contribuição estão grandes demais; deixe-os com 12x12 px.”*
- *“Adicione uma dica ao passar o cursor que mostre a data e a quantidade de contribuições.”*
- *“O estado de carregamento precisa de uma animação pulsante.”*

<!-- track:vscode:start -->
O Agent Mode lida naturalmente com alterações em vários arquivos e iterações. Cada prompt de acompanhamento usa o contexto da conversa anterior, permitindo refinar a implementação aos poucos sem começar do zero.
<!-- track:vscode:end -->

<!-- track:cli:start -->
As sessões do Copilot CLI mantêm o histórico, então cada prompt de acompanhamento se baseia nos anteriores. Use `/session` ou `/context` para inspecionar o contexto mantido pelo Copilot e `/review` depois de uma iteração maior para procurar erros ou melhorias.
<!-- track:cli:end -->

## Dicas para esta parte

- **Seja específico sobre o que você quer** — requisitos claros levam a resultados melhores.
- **Divida tarefas grandes em prompts menores** se o Copilot sair do rumo.
- **Revise as alterações antes de aceitá-las** — inspecionar o código gerado é mais rápido do que reescrevê-lo depois.
- **Teste o aplicativo após cada implementação** para detectar os problemas enquanto ainda são pontuais.

## ✅ Parte 3 concluída

Você aprendeu a:

- Usar o Copilot para **implementar alterações em vários arquivos**.
- **Iterar nos resultados** com feedback de acompanhamento específico.
- Conduzir o **ciclo completo de uma funcionalidade** — implementação, revisão, teste e refinamento.
