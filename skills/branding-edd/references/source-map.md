# Mapa de fontes - Branding EDD

## GitHub

Fonte canônica: repositório `Brand-System`, pasta `EDD-Brand-System/`.

Resolução preferida:
1. procurar `Brand-System` na organização Complan;
2. confirmar `EDD-Brand-System/AGENTS.md`;
3. se ainda não estiver transferido, usar `agenciacomplan-pixel/Brand-System`.

Arquivos principais:
- `EDD-Brand-System/AGENTS.md`
- `EDD-Brand-System/BRAND.md`
- `EDD-Brand-System/DESIGN-TOKENS.json`
- `EDD-Brand-System/guidelines/`
- `EDD-Brand-System/references/drive-sources.json`
- `EDD-Brand-System/references/reference-index.json`
- `EDD-Brand-System/references/reference-insights.md`
- `EDD-Brand-System/docs/decisions.md`

## Google Drive

Biblioteca viva da EDD:
`https://drive.google.com/drive/folders/17G5OWGdbW1p4a1FidR6tJ6tcYCSxEtnV`

Não duplicar a biblioteca inteira dentro da Skill. Usar as pastas e IDs documentados em `drive-sources.json` e `reference-index.json`.

## Regra de sincronização

A chave de comparação é:
- `file_id`
- `modified_time`

Sem mudança: usar insights consolidados e não reabrir imagens.
Com mudança: analisar somente o delta, classificar o contexto, atualizar índice/insights quando houver permissão e só depois criar.

## Transferência futura

A Skill não deve depender permanentemente do owner `agenciacomplan-pixel`. Depois que o repositório for transferido para a organização Complan, resolver novamente pelo nome `Brand-System` + presença de `EDD-Brand-System/AGENTS.md`.
