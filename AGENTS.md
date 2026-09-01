# AGENTS.md - Brand System

Este repositório é a fonte central de sistemas de marca. Cada marca possui sua própria pasta e regras específicas.

## Regra de escopo

Antes de produzir, editar ou revisar qualquer material de uma marca:

1. Identifique a marca correta.
2. Leia o arquivo `BRAND.md` dentro da pasta da marca.
3. Leia apenas as guidelines relevantes ao tipo de entrega.
4. Consulte `references/reference-insights.md` antes de usar referências visuais.
5. Consulte `references/reference-index.json` antes de reabrir referências do Google Drive.

## Atualização incremental de referências

Nunca reprocessar toda a biblioteca visual por padrão.

Antes de criar uma nova peça:

1. Verifique metadados das pastas monitoradas no Google Drive.
2. Compare `file_id` + `modified_time` com `reference-index.json`.
3. Se não houver arquivos novos ou modificados, não reabra as imagens já analisadas.
4. Se houver arquivos novos ou modificados, analise somente o delta.
5. Atualize `reference-index.json` e `reference-insights.md` antes da criação.
6. Só altere uma regra estrutural em `BRAND.md` quando houver evidência recorrente ou decisão explícita da responsável pela marca.

Uma referência nova não vira regra automaticamente.

## Pastas vazias

Uma pasta vazia significa apenas ausência de evidência atual. Não interpretar uma pasta vazia como aprovação irrestrita nem inventar regras com base nela.

## Hierarquia de fontes de verdade

Em caso de conflito, seguir esta ordem:

1. Decisões explícitas e mais recentes da responsável pela marca.
2. `BRAND.md` e guidelines consolidadas.
3. Design tokens oficiais.
4. Referências positivas recentes já analisadas.
5. Manual de identidade mais antigo.
6. Liberdade criativa, sempre dentro das regras acima.

## Princípio de não cópia

Referências servem para extrair princípios, direção, ritmo, composição e linguagem. Não copiar layouts de terceiros nem reproduzir peças de forma literal.

## Regra de variedade criativa

Quando forem solicitadas múltiplas opções, as opções devem explorar direções visuais genuinamente diferentes, mantendo o mesmo núcleo de marca. Evitar entregar apenas variações superficiais de posição, foto ou cor.

## Website

O sistema de marca deve se aplicar ao web sem transformar o site em um post ampliado. Componentes web devem considerar hierarquia, responsividade, acessibilidade, estados de interação, legibilidade e consistência com o núcleo visual da marca.
