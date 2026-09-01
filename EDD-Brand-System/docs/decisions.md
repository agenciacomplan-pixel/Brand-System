# Decisões de Brand System - EDD

## 2026-08-31 - Estrutura inicial

- Criar um repositório central `Brand-System` para reunir várias marcas.
- A EDD é a primeira marca e fica em `EDD-Brand-System/`.
- O Google Drive permanece como biblioteca viva de mídia.
- O GitHub guarda regras, tokens, índices, insights e decisões.
- Referências não devem ser reprocessadas integralmente a cada criação.
- A detecção de mudanças usa `file_id` + `modified_time`.
- Antes de criar uma nova peça, qualquer referência nova/modificada deve ser analisada e os insights atualizados.
- Uma nova referência não altera automaticamente uma regra estrutural da marca.
- Pastas vazias significam ausência de evidência, não ausência de restrições.
- A pasta `Peças que não gosto` está vazia na linha de base.
- A pasta `Referências Externas` está vazia na linha de base.
- O site atual é referência provisória de conteúdo, negócio e estrutura, não padrão visual definitivo.
- Quando forem pedidas várias opções de peça, elas devem representar direções criativas materialmente distintas.
- Para professores e pessoas reais, priorizar fotos reais do Drive e preservar fisionomia.

## 2026-08-31 - Consolidação visual inicial

- Realizada análise visual da carga inicial de 13 posts e 13 capas de Reels.
- As referências foram convertidas em insights condensados para evitar releitura integral futura.
- A partir desta linha de base, o processo passa a ser incremental.
- Fundos claros, escuros, fotografia dominante, mockups, cards, tipografia em grande escala e composições editoriais são possibilidades compatíveis com a EDD.
- Recursos recorrentes são permissões criativas e não obrigatoriedades de layout.
- Soluções visuais de campanha devem ser classificadas antes de virar regra geral.
- Preto + verde observado em contexto `Black` permanece contextual.
- Laranja dominante observado em peça isolada não foi promovido a cor central.
- Fontes script observadas em conteúdo comemorativo permanecem contextuais.

## 2026-08-31 - Sala de Aprendizado

- `Sala de Aprendizado` é um módulo específico da EDD.
- Suas referências não devem alimentar automaticamente o repertório criativo geral.
- A linguagem da Sala de Aprendizado só pode ser ativada quando o pedido mencionar explicitamente o módulo ou o contexto for inequívoco.
- Em pedidos genéricos, a Sala de Aprendizado não deve ser oferecida como uma das opções criativas.
- Criada guideline exclusiva `guidelines/sala-de-aprendizado.md`.
- A pasta do módulo foi adicionada ao índice incremental do Drive.
- As 3 referências iniciais do módulo foram analisadas separadamente.
- Uma peça que também aparece em `Capas de Reels` foi classificada como `Sala de Aprendizado`, e essa classificação contextual prevalece sobre o uso como referência geral.
- Amarelo vivo e a arquitetura específica de gradiente/nome do módulo não foram promovidos à identidade geral da EDD.

## 2026-08-31 - Checagem diária do Drive

- Para reduzir chamadas e consumo desnecessário de contexto, a EDD passa a fazer no máximo uma checagem automática de mudanças no Google Drive por dia, usando `America/Sao_Paulo`.
- O estado compartilhado fica em `references/sync-state.json`.
- Se o Drive já foi checado no dia, novos pedidos de criação reutilizam os insights consolidados e não consultam novamente as pastas do Drive.
- A regra é anulada no mesmo dia quando o usuário informar que subiu, alterou ou removeu referências/assets, pedir atualização do repertório ou sincronização, ou quando a tarefa depender de um arquivo recém-adicionado.
- Quando a checagem for necessária, continua valendo a análise apenas por delta usando `file_id` + `modified_time`.
- Para o estado diário funcionar entre chats e contas do workspace, a execução que fizer a primeira checagem do dia deve conseguir atualizar `sync-state.json` no GitHub.

## Próximas decisões futuras

Registrar aqui, com data, qualquer mudança em paleta, tipografia, direção visual, web, fotografia, logo, módulos contextuais ou processo de atualização de referências.
