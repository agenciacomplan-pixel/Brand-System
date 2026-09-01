# AGENTS.md - EDD

Escopo: tudo dentro de `EDD-Brand-System/` pertence à **EDD - Escola de Dança Louvor na Terra**.

## Antes de qualquer criação visual

1. Leia `BRAND.md`.
2. Leia `DESIGN-TOKENS.json`.
3. Leia somente a guideline relevante ao formato solicitado.
4. Leia `references/reference-insights.md`.
5. Consulte `references/sync-state.json` antes de decidir se o Google Drive precisa ser checado.
6. Consulte `references/reference-index.json` quando houver checagem necessária ou quando a tarefa depender de uma referência específica.

## Regra de checagem diária do Drive

Usar a data de `America/Sao_Paulo`.

- Se `references/sync-state.json` indicar que o Drive já foi checado na data atual, NÃO consultar o Drive novamente naquele dia.
- Reutilizar `reference-index.json` e `reference-insights.md` nas demais criações do mesmo dia.
- Forçar nova checagem no mesmo dia somente se o usuário disser que adicionou, removeu ou alterou referências/assets, pedir explicitamente nova sincronização/checagem ou se a tarefa depender de um arquivo recém-adicionado.
- Na primeira checagem necessária do dia, comparar `file_id` + `modified_time` e analisar somente o delta.
- Após checagem bem-sucedida, atualizar `sync-state.json` para compartilhar o estado entre chats e contas do workspace.
- Nunca reabrir imagens inalteradas apenas para confirmar que continuam iguais.

## Regra obrigatória de sincronização quando houver checagem

- Se nenhum `file_id` novo aparecer e nenhum `modified_time` mudar, NÃO reabra as imagens antigas.
- Se houver arquivo novo ou modificado, analise somente esse delta.
- Atualize `reference-index.json` e `reference-insights.md` antes de iniciar a nova criação.
- Não transformar uma referência isolada em regra estrutural automaticamente.

## Sala de Aprendizado: contexto fechado

- **Sala de Aprendizado é um módulo específico da EDD, não uma direção criativa geral da marca.**
- Elementos, padrões, layouts, selos, nomenclaturas ou linguagem visual identificados como pertencentes à Sala de Aprendizado só podem ser usados quando o pedido mencionar explicitamente `Sala de Aprendizado` ou deixar inequívoco que a peça pertence a esse módulo.
- Ao analisar referências existentes, classificar peças de Sala de Aprendizado separadamente e não usá-las para inferir regras gerais de posts, anúncios, capas ou páginas da EDD.
- Em um pedido genérico da EDD, nunca escolher a linguagem da Sala de Aprendizado como uma das opções criativas por conta própria.

## Seleção de pessoas

- Conteúdo sobre professor específico: usar fotos reais da pasta correspondente.
- Professor relevante mas não informado: perguntar qual professor usar.
- Conteúdo institucional sem pessoa específica: selecionar grupo ou imagem institucional adequada.
- Não substituir pessoas reais por rostos inventados quando houver material real disponível.
- Preservar fisionomia e características reconhecíveis.

## Múltiplas opções

Quando forem pedidas várias opções, criar direções realmente distintas dentro da marca. Priorizar diferenças de conceito e composição, não apenas troca de foto, cor ou posição.

## Web

Enquanto não houver novas referências de site aprovadas, usar o site atual apenas para compreender conteúdo, negócio e estrutura. Não copiá-lo visualmente nem tratá-lo como padrão definitivo.

## Pastas sem conteúdo

`Peças que não gosto` e `Referências Externas` estavam vazias na linha de base inicial. Se passarem a conter arquivos, isso é delta prioritário e deve ser analisado na próxima checagem do Drive ou imediatamente quando o usuário informar a mudança.

## Integridade da marca

Na dúvida entre inventar uma regra e pedir uma decisão de marca, pedir a decisão. Registrar decisões relevantes em `docs/decisions.md`.
