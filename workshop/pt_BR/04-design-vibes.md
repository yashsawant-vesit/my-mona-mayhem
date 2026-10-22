<!-- l10n-sync: source-file="workshop/04-design-vibes.md" -->
# Parte 4: Tematização orientada pelo design

---

Nesta parte, você vai usar os ciclos de planejamento e implementação do Copilot para projetar uma transformação completa do tema. Esta é uma abordagem de desenvolvimento orientada pelo design: comece com a visão, itere nos elementos visuais e deixe o Copilot cuidar do trabalho pesado de CSS.

## Tarefa 1: Planeje o tema retrô

<!-- track:vscode:start -->
Mude para o modo **Plan** no GitHub Copilot Chat.
<!-- track:vscode:end -->

<!-- track:cli:start -->
Use `/plan` no GitHub Copilot CLI ou pressione **Shift+Tab** até ativar o modo de planejamento.
<!-- track:cli:end -->

Digite este prompt:

> Quero transformar esta página em uma experiência completa de fliperama retrô. Planeje uma reformulação visual abrangente que inclua: efeitos de linhas de varredura CRT no fundo, brilho neon no título pulsando como um letreiro, selo VS animado com mudanças nas cores do gradiente, sobreposição de brilho/cintilação nos cartões de resultado dos usuários, animações de entrada flutuante nos campos, texto de carregamento alternando entre verde e roxo e efeitos de brilho ao passar o cursor sobre os quadrados de contribuição. Mantenha o fundo escuro (`#0a0a1a`) com as cores de destaque verde (`#5fed83`) e roxo (`#8a2be2`). Use um tema escuro com a fonte retrô Press Start 2P do Google Fonts.

O Copilot vai gerar um plano detalhado de implementação que abrange todos os efeitos visuais. **Não aceite imediatamente** — revise o plano e itere:

- Sugira ajustes na duração das animações (por exemplo: “Deixe o pulso neon mais lento, com cerca de 3 segundos”).
- Pergunte sobre efeitos específicos (por exemplo: “Como funcionará a sobreposição cintilante nos cartões?”).
- Peça mudanças na abordagem se algo não parecer adequado.

## Tarefa 2: Implemente o tema

Quando estiver satisfeito com o plano, peça ao Copilot para implementá-lo.

> Implemente o plano do tema de fliperama retrô que acabamos de criar.

O Copilot vai adicionar várias animações CSS, pseudoelementos e transições à sua folha de estilos. Isso pode incluir:

- `@keyframes` para linhas de varredura, pulso neon, cintilação e efeitos de entrada flutuante.
- Pseudoelementos (`::before`, `::after`) para efeitos de sobreposição.
- Propriedades personalizadas de CSS para as cores do tema.
- Transições e estados de hover para elementos interativos.

<!-- track:cli:start -->
Quando as alterações forem aplicadas, use `/diff` para revisar os estilos antes de aprová-los.
<!-- track:cli:end -->

## Tarefa 3: Ajuste os detalhes visuais

> **⚠️ Não está vendo as alterações?** Se o novo tema ou as animações não aparecerem, pare o servidor de desenvolvimento (`Ctrl+C`), reinicie com `npm run dev` e force a atualização do navegador (`Ctrl+Shift+R`).

Mantenha a pré-visualização do navegador aberta e itere no design. Experimente prompts como:

> O efeito de linhas de varredura está forte demais; reduza a opacidade para 0.03.

> Adicione uma cintilação elétrica sutil ao texto do título.

> O selo VS deve pulsar com mais intensidade.

Esta é uma abordagem de **desenvolvimento orientada pelo design** — você está iterando no resultado visual em tempo real. Cada prompt refina a experiência até ela ficar do jeito certo. Não se contente com “bom o suficiente” — aperfeiçoe o visual até a página parecer parte de um fliperama.

## Tarefa 4: Atualize as instruções

Suas instruções devem refletir decisões importantes de design para orientar os próximos prompts.

<!-- track:vscode:start -->
Peça ao Copilot Chat:

> Adicione uma seção de guia de design ao copilot-instructions.md descrevendo nosso tema de fliperama retrô: cores, fontes e estilo das animações.
<!-- track:vscode:end -->

<!-- track:cli:start -->
Peça ao Copilot CLI:

> Atualize as instruções do repositório com um breve guia de design para o tema de fliperama retrô: cores, fontes, estilo das animações e a regra de que novas interfaces devem manter a estética neon.
<!-- track:cli:end -->

Quando a página estiver como você quer, faça commit das instruções atualizadas e das alterações de design.

## ✅ Parte 4 concluída

**O que você aprendeu:**

- Usar fluxos de planejamento para esboçar um **sistema de design antes de implementá-lo**.
- **Iterar no resultado visual** com prompts rápidos de acompanhamento.
- **Atualizar as instruções após decisões importantes** para manter a identidade visual.
