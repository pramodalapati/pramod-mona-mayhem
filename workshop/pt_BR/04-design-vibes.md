<!-- l10n-sync: source-file="workshop/04-design-vibes.md" -->
# Parte 4: Tema orientado a design

---

Nesta parte, você vai usar os ciclos de planejamento e implementação do Copilot para projetar uma transformação completa do tema. A abordagem começa pelo design: defina a visão, itere nos elementos visuais e deixe o Copilot cuidar do trabalho pesado de CSS.

## Tarefa 1: Planeje o tema retrô

<!-- track:vscode:start -->
Mude para o modo **Plan** no GitHub Copilot Chat.
<!-- track:vscode:end -->

<!-- track:cli:start -->
Execute `/plan` no GitHub Copilot CLI ou pressione **Shift+Tab** até ativar o modo de planejamento.
<!-- track:cli:end -->

Digite este prompt:

> Quero transformar esta página em uma experiência completa de fliperama retrô. Planeje uma reformulação visual abrangente que inclua: efeitos de linhas de varredura CRT no plano de fundo, brilho neon pulsante no título, selo VS animado com mudanças de cor no gradiente, sobreposição de brilho nas fichas de resultado dos usuários, animações de entrada flutuante nos campos, texto de carregamento que alterne entre verde e roxo e efeitos de brilho ao passar o cursor sobre os quadrados de contribuições. Mantenha o plano de fundo escuro (`#0a0a1a`) e as cores de destaque verde (`#5fed83`) e roxo (`#8a2be2`). Use um tema escuro com a fonte retrô Press Start 2P do Google Fonts.

O Copilot vai gerar um plano detalhado com todos os efeitos visuais. **Não aceite imediatamente**: revise o plano e itere:

- Sugira ajustes no tempo das animações (por exemplo: *“Deixe a pulsação neon mais lenta, em torno de 3 segundos.”*).
- Pergunte sobre efeitos específicos (por exemplo: *“Como a sobreposição de brilho funcionará nas fichas?”*).
- Peça mudanças na abordagem se algo não parecer certo.

## Tarefa 2: Implemente o tema

Quando estiver satisfeito com o plano, peça ao Copilot para implementá-lo:

> Implemente o plano do tema de fliperama retrô que acabamos de criar.

O Copilot vai adicionar várias animações CSS, pseudo-elementos e transições à folha de estilos. Isso pode incluir:

- `@keyframes` para linhas de varredura, pulsação neon, brilho e efeitos de entrada flutuante
- Pseudo-elementos (`::before`, `::after`) para efeitos de sobreposição
- Propriedades personalizadas de CSS para as cores do tema
- Transições e estados de hover para elementos interativos

<!-- track:cli:start -->
Quando as alterações forem aplicadas, use `/diff` para revisar os estilos antes de aprová-los.
<!-- track:cli:end -->

## Tarefa 3: Ajuste os detalhes visuais

> **⚠️ Não está vendo as alterações?** Se o novo tema ou as animações não aparecerem, pare o servidor (`Ctrl+C`), reinicie-o com `npm run dev` e atualize o navegador sem usar o cache (`Ctrl+Shift+R`).

Mantenha a pré-visualização no navegador aberta e itere no design. Experimente prompts como:

> O efeito de linhas de varredura está forte demais; reduza a opacidade para 0.03.

> Adicione uma oscilação elétrica sutil ao título.

> O selo VS deve pulsar de forma mais intensa.

Esta é uma abordagem de **desenvolvimento orientado a design**: você itera no resultado visual em tempo real. Cada prompt refina a experiência até que ela fique como você deseja. Não se contente com “bom o suficiente”: continue ajustando até a página parecer parte de um fliperama.

## Tarefa 4: Atualize as instruções

Suas instruções devem refletir as principais decisões de design para manter os próximos prompts alinhados.

<!-- track:vscode:start -->
Peça ao Copilot Chat:

> Adicione a `copilot-instructions.md` uma seção de guia de design que descreva o tema de fliperama retrô: cores, fontes e estilo das animações.
<!-- track:vscode:end -->

<!-- track:cli:start -->
Peça ao Copilot CLI:

> Atualize as instruções do repositório com um breve guia de design para o tema de fliperama retrô: cores, fontes, estilo das animações e a regra de que novas interfaces devem manter a estética neon.
<!-- track:cli:end -->

Quando a página estiver como você deseja, faça commit das instruções atualizadas e das alterações de design.

## ✅ Parte 4 concluída

**O que você aprendeu:**

- Usar fluxos de planejamento para esboçar um **sistema de design antes da implementação**
- **Iterar no resultado visual** com prompts de acompanhamento
- **Atualizar as instruções após decisões importantes** para manter uma identidade visual consistente
