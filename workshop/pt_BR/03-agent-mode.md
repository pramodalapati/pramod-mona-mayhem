<!-- l10n-sync: source-file="workshop/03-agent-mode.md" -->
# Parte 3: Construa o jogo com fluxos de trabalho com agentes

---

Nesta parte, o Copilot passa do planejamento à implementação. Em vez de escrever código linha por linha, você descreve o que precisa e deixa o Copilot realizar as alterações nos arquivos necessários.

## Tarefa 1: Conecte a batalha

<!-- track:vscode:start -->
1. Mude para o modo **Agent** no Copilot Chat.
2. Digite este prompt:
<!-- track:vscode:end -->

<!-- track:cli:start -->
1. Volte ao fluxo normal de programação do Copilot CLI (ou permaneça no modo autopilot se quiser que o Copilot continue até você interrompê-lo).
2. Se for útil, mencione o arquivo da página para dar mais contexto: `@src/pages/index.astro`.
3. Digite este prompt:
<!-- track:cli:end -->

   > Adicione JavaScript do lado do cliente à página de batalha para que:
   > 1. Ao clicar no botão Battle, obtenha os dois nomes de usuário dos campos.
   > 2. Valide se ambos foram preenchidos e exiba um erro caso contrário.
   > 3. Busque em paralelo os dados de contribuições dos dois usuários pela nossa API.
   > 4. Renderize os gráficos de contribuições em grades coloridas, com um quadrado colorido por dia usando a paleta do GitHub.
   > 5. Exiba um selo VS entre os dois usuários.
   > 6. Mostre o nome de usuário, o total de contribuições e o intervalo de datas de cada usuário.
   > 7. Gerencie os estados de carregamento e os erros.
   > 8. Também inicie a batalha ao pressionar Enter nos campos.
   > 9. Use a interface simples que já está estruturada.
   >
   > Use interfaces do TypeScript para a estrutura dos dados de contribuições.

<!-- track:vscode:start -->
3. Deixe o Agent Mode implementar as alterações em `index.astro`.
4. Revise as alterações propostas na visualização de diff antes de aceitá-las.
<!-- track:vscode:end -->

<!-- track:cli:start -->
4. Deixe o Copilot CLI implementar as alterações em `src/pages/index.astro`.
5. Use `/diff` para inspecionar e aprovar as alterações geradas.
<!-- track:cli:end -->

## Tarefa 2: Teste a batalha

> **⚠️ Não está vendo as alterações?** Se a página de batalha não tiver sido atualizada, pare o servidor (`Ctrl+C`), reinicie-o com `npm run dev` e atualize o navegador.

1. Digite `octocat` e `torvalds` como nomes de usuário e clique em **Battle**.
2. Os dois gráficos de contribuições devem aparecer lado a lado em grades coloridas.
3. Teste também os casos de erro:
   - Deixe um ou ambos os campos vazios e clique em Battle: deve aparecer um erro de validação.
   - Digite um nome de usuário inválido: o app deve exibir um erro da API.
4. Pressione **Enter** em qualquer campo: a batalha deve começar como se você tivesse clicado no botão.

## Tarefa 3: Itere com o Copilot

Se algo não estiver como esperado, envie comentários de acompanhamento diretamente ao Copilot. Por exemplo:

- *“Os quadrados de contribuições estão grandes demais; reduza-os para 12x12px.”*
- *“Adicione uma dica ao passar o cursor que mostre a data e a quantidade de contribuições.”*
- *“O estado de carregamento precisa de uma animação de pulsação.”*

<!-- track:vscode:start -->
O Agent Mode lida naturalmente com alterações em vários arquivos e com iterações. Cada prompt de acompanhamento aproveita a conversa anterior para que você refine a implementação aos poucos, sem começar do zero.
<!-- track:vscode:end -->

<!-- track:cli:start -->
As sessões do Copilot CLI mantêm o histórico, então cada prompt de acompanhamento aproveita o anterior. Use `/session` ou `/context` para inspecionar o contexto que o Copilot está usando e `/review` após uma iteração maior para fazer uma revisão extra de bugs ou pontos a polir.
<!-- track:cli:end -->

## Dicas para esta parte

- **Seja específico sobre o que você quer**: requisitos claros levam a resultados melhores.
- **Divida tarefas grandes em prompts menores** se o Copilot sair do rumo.
- **Revise as alterações antes de aceitá-las**: é mais rápido inspecionar o código gerado do que reescrevê-lo depois.
- **Teste o app após cada etapa de implementação** para detectar problemas rapidamente.

## ✅ Parte 3 concluída

Você aprendeu a:

- Usar o Copilot para **implementar alterações em vários arquivos**
- **Iterar nos resultados** com comentários de acompanhamento específicos
- Concluir o **ciclo completo de desenvolvimento**: implementação, revisão, testes e refinamento
