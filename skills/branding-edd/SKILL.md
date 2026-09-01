---
name: branding-edd
description: Aplica e mantém o Brand System da EDD (Escola de Dança Louvor na Terra) em posts, capas de Reels, anúncios, páginas, sites, apresentações e outras peças visuais. Use quando o usuário pedir algo “no branding da EDD”, “no estilo da EDD”, mencionar EDD/Escola de Dança Louvor na Terra, Sala de Aprendizado, professor da EDD, ou solicitar criação/revisão visual que deva seguir a marca. Coordena GitHub + Google Drive, usa checagem diária compartilhada para evitar consultas repetidas, verifica referências novas por delta e preserva contextos fechados como Sala de Aprendizado.
---

# Branding EDD

Usar o Brand System vivo da **EDD - Escola de Dança Louvor na Terra** como fonte de verdade. Não congelar o branding dentro desta Skill: as regras oficiais permanecem no GitHub e a biblioteca de mídia permanece no Google Drive.

## Fluxo obrigatório

1. **Resolver a fonte oficial no GitHub.**
   - Procurar um repositório acessível chamado `Brand-System` que contenha `EDD-Brand-System/AGENTS.md`.
   - Se houver mais de um, preferir a versão na organização Complan quando existir.
   - Enquanto a transferência não ocorrer, a fonte conhecida é `agenciacomplan-pixel/Brand-System`.
   - Nunca assumir que um repositório com mesmo nome é o correto sem confirmar a existência de `EDD-Brand-System/AGENTS.md`.

2. **Carregar somente o necessário.**
   Ler, nesta ordem:
   - `EDD-Brand-System/AGENTS.md`
   - `EDD-Brand-System/BRAND.md`
   - `EDD-Brand-System/DESIGN-TOKENS.json`
   - a guideline específica do formato solicitado
   - `EDD-Brand-System/references/reference-insights.md`
   - `EDD-Brand-System/references/sync-state.json`
   - `EDD-Brand-System/references/reference-index.json` somente quando houver checagem necessária ou quando a tarefa depender de uma referência específica
   - `docs/decisions.md` somente quando houver dúvida de governança ou evolução de marca.

3. **Aplicar a janela de checagem diária antes de consultar o Drive.**
   - Ler primeiro `EDD-Brand-System/references/sync-state.json`.
   - Usar a data de `America/Sao_Paulo` como referência do dia.
   - Se `last_drive_check_date` for igual à data atual, **não consultar o Google Drive novamente naquele dia**. Usar `reference-index.json` + `reference-insights.md` já consolidados.
   - Forçar nova checagem no mesmo dia somente quando o usuário disser ou implicar claramente que adicionou, removeu ou alterou referências/assets no Drive, pedir explicitamente uma nova checagem/sincronização, ou quando uma tarefa depender de um arquivo específico recém-enviado.
   - Se `last_drive_check_date` for diferente da data atual ou estiver vazio, fazer a checagem normal do Drive.
   - Na checagem normal, usar `references/drive-sources.json` e `reference-index.json`, comparar `file_id` + `modified_time` e analisar somente arquivos novos ou modificados.
   - Após uma checagem bem-sucedida, atualizar `sync-state.json` com a data atual e, se possível, o horário da checagem.
   - Nunca reabrir referências visuais inalteradas apenas para confirmar o estado.

4. **Classificar o delta antes de aprender com ele.**
   Classificar cada referência nova/modificada como uma destas categorias:
   - `general-edd`
   - `campaign-contextual`
   - `sala-de-aprendizado`
   - `negative-reference`
   - `external-reference`
   - `asset-only`

5. **Atualizar o sistema quando houver permissão.**
   - Após checar o Drive, atualizar `sync-state.json` para que outros chats e contas do workspace possam reutilizar a checagem do mesmo dia.
   - Atualizar `reference-index.json` com o novo estado.
   - Atualizar `reference-insights.md` com aprendizados condensados relevantes.
   - Não promover uma referência isolada a regra estrutural de `BRAND.md` automaticamente.
   - Só alterar `BRAND.md` quando houver padrão recorrente ou decisão explícita do responsável pela marca.
   - Registrar decisões estruturais em `docs/decisions.md`.
   - Se a conta atual não tiver permissão de escrita no GitHub, usar o delta na tarefa atual e informar claramente que a sincronização central ficou pendente. Nunca afirmar que atualizou quando não atualizou.

6. **Resolver o briefing mínimo antes de criar.**
   - Se o pedido visual estiver genérico e não informar formato, canal ou dimensão, perguntar **qual dimensão/formato o usuário quer** antes de gerar a peça. Fazer uma pergunta curta, sem iniciar a criação ainda.
   - Não perguntar de novo quando o formato já estiver explícito ou puder ser inferido com segurança pelo canal.
   - Defaults da EDD para social:
     - feed do Instagram: `4:5`;
     - carrossel de feed: `4:5` por página;
     - Stories: `9:16`;
     - capa de Reels: `9:16`.
   - Se o usuário disser apenas “post”, “arte”, “imagem”, “peça” ou equivalente sem canal/dimensão, perguntar o formato desejado.
   - Para banners, anúncios, thumbnails, apresentações ou web sem destino/tamanho claro, perguntar o formato/destino relevante em vez de inventar dimensões.
   - **Capa de Reels:** antes de buscar uma foto no banco/Drive ou gerar imagem, perguntar se o usuário tem um print/frame do próprio vídeo que deseja usar na capa. Se já houver um frame anexado na conversa, priorizá-lo e não perguntar novamente. Se o usuário disser que não tem ou preferir outra imagem, então selecionar fotografia real adequada no Drive ou seguir a direção solicitada.

7. **Criar ou revisar a peça.**
   - Aplicar a guideline do formato e os insights consolidados.
   - Priorizar reconhecimento de marca sem repetir um único template.
   - Quando o usuário pedir várias opções, produzir direções visualmente distintas, não pequenas variações do mesmo layout.

## Contextos fechados

### Sala de Aprendizado

Tratar **Sala de Aprendizado** como módulo específico da EDD, não como direção criativa geral.

- Só carregar `guidelines/sala-de-aprendizado.md` quando o pedido mencionar explicitamente `Sala de Aprendizado` ou for inequivocamente sobre esse módulo.
- Nunca oferecer a linguagem da Sala de Aprendizado como opção em um pedido genérico da EDD.
- Referências classificadas como Sala de Aprendizado não alimentam o repertório geral, mesmo quando também estiverem em outra pasta como Capas de Reels.
- Elementos exclusivos do módulo, como amarelo de destaque ou arquitetura específica de layout, não viram regra geral da EDD.

### Campanhas específicas

Não transformar linguagem de campanha em identidade permanente. Exemplos já registrados no Brand System incluem Black, peças comemorativas e soluções cromáticas pontuais.

## Pessoas e fotografia

- Para professor específico, consultar a pasta real daquele professor.
- Se a escolha do professor impactar a mensagem e o usuário não informar quem é, perguntar qual professor usar.
- Para comunicação institucional sem pessoa específica, priorizar grupo ou foto institucional adequada.
- Não inventar um rosto de professor quando houver foto real disponível.
- Preservar fisionomia e características reconhecíveis de pessoas reais.
- Escolher orientação e enquadramento adequados ao formato final.

## Criação de imagem

Antes de chamar a ferramenta de geração/edição de imagem, cumprir o briefing mínimo de formato/dimensão acima. Quando a tarefa pedir uma imagem, usar a ferramenta disponível no ambiente após carregar as regras da marca e resolver os assets relevantes. Não tentar reproduzir visualmente uma referência externa de forma literal; extrair princípios de composição e direção.

## Web e site

Para site, landing page ou interface:

- Ler `guidelines/web.md`.
- Tratar o site atual `https://dancalouvornaterra.com.br/` como referência provisória de conteúdo, negócio e estrutura, não como padrão visual definitivo.
- Aplicar o núcleo da EDD em tipografia, fotografia, cor e hierarquia sem transformar o site em um “post gigante”.
- Quando novas referências web forem aprovadas no Drive, incorporá-las pelo fluxo incremental antes de definir novas regras.

## Referências negativas e externas

- Pasta vazia significa **ausência de evidência**, não liberdade irrestrita.
- Quando `Peças que não gosto` ganhar novos arquivos, analisar apenas o delta e registrar o motivo visual provável da rejeição.
- Quando `Referências Externas` ganhar novos arquivos, extrair princípios úteis sem copiar layouts.
- Não alterar regras estruturais por uma única referência nova sem recorrência ou decisão explícita.

## Governança de workspace

Esta Skill é projetada para uso compartilhado no workspace.

- Não depender de memória pessoal de uma única conta.
- Toda regra importante deve estar no Brand System central, não apenas na conversa.
- Cada usuário precisa ter acesso aos conectores/fontes necessários para leitura. Para compartilhar o estado de checagem diária entre chats e contas, a integração que executar a primeira checagem do dia precisa conseguir atualizar `references/sync-state.json` no GitHub.
- Se GitHub ou Drive não estiverem acessíveis, informar a limitação e não inventar branding, referências ou atualizações.

## Exemplos de acionamento

- “Use o branding da EDD e crie 3 opções de post para uma nova turma.”
- “Faça uma capa de Reels da EDD sobre desenho coreográfico.”
- “Crie uma peça da Sala de Aprendizado com a professora X.”
- “Monte a home do novo site da EDD seguindo o Brand System.”
- “Revise esta arte e diga o que está fora do branding da EDD.”

## Recursos da Skill

- Ler `references/briefing-policy.md` quando o pedido visual estiver incompleto ou envolver capa de Reels.
- Ler `references/daily-sync-policy.md` para a regra de cache diário e gatilhos de rechecagem.
- Ler `references/source-map.md` quando precisar localizar as fontes atuais e entender a lógica de transferência do repositório.
- Ler `references/quality-checklist.md` antes de finalizar uma peça ou uma recomendação visual complexa.
