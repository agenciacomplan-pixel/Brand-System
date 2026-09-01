# Política de sincronização diária - EDD

## Objetivo

Reduzir chamadas repetidas ao Google Drive e consumo desnecessário de contexto sem perder a capacidade de incorporar referências novas.

## Estado compartilhado

Usar `EDD-Brand-System/references/sync-state.json` no repositório canônico. A data oficial do ciclo diário é `America/Sao_Paulo`.

## Regra

1. Ler `sync-state.json` antes de listar qualquer pasta do Drive.
2. Se `last_drive_check_date` for igual à data atual em São Paulo, pular toda checagem de mudanças no Drive.
3. Se a data for antiga ou vazia, listar metadados das pastas monitoradas, comparar com `reference-index.json` e analisar somente o delta.
4. Após checagem concluída, gravar a data atual em `last_drive_check_date`.

## Gatilhos que anulam o cache no mesmo dia

Checar novamente imediatamente se o usuário disser algo equivalente a:

- “subi uma imagem/referência”;
- “adicionei arquivos no Drive”;
- “mudei uma referência”;
- “coloquei algo em Peças que não gosto”;
- “adicionei referência externa”;
- “atualizei as fotos do professor”;
- “atualize o repertório”;
- “sincronize novamente”;
- “cheque o Drive de novo”.

Também forçar quando a tarefa depender explicitamente de um arquivo que o usuário acabou de adicionar.

## O que não força rechecagem

Novos pedidos de posts, capas, anúncios, páginas ou variações criativas no mesmo dia, sem indicação de mudança nas fontes, devem reutilizar o estado do dia.

## Limitação

Para o cache valer entre chats e contas do workspace, a primeira execução que checar o Drive precisa ter permissão de escrita no GitHub para atualizar `sync-state.json`. Sem essa permissão, manter o cache apenas no contexto disponível e não afirmar que o estado compartilhado foi atualizado.
