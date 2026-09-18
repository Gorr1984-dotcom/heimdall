# Catálogo de plugins do Claude Code

Fonte: [quemsah/awesome-claude-plugins](https://github.com/quemsah/awesome-claude-plugins)
(Top 100, lista de 13.09.2026) mais [obra/superpowers-marketplace](https://github.com/obra/superpowers-marketplace).

- Marketplaces catalogados: **95**
- Plugins catalogados: **886**
- Marketplaces registrados em `.claude/settings.json`: **5**
- Plugins habilitados: **0**

Os nomes saíram do `.claude-plugin/marketplace.json` de cada repositório, baixado
e validado — não são suposição.

## Política adotada

Este arquivo é índice, não configuração: ele não entra no contexto de nenhuma
sessão, então catalogar 886 plugins não custa token nenhum.

O que custa fica fora dele:

- **Registrar** um marketplace faz o Claude Code clonar aquele repositório para
  ler o manifesto. Token zero, mas disco e latência de startup — e a lista Top 100
  é ordenada por estrelas, então inclui monorepos como `next.js`, `storybook`,
  `diffusers` e `ccxt`, clonados só para extrair um JSON de 2 KB. Por isso
  `extraKnownMarketplaces` tem apenas 5 entradas:
  `superpowers-marketplace`, `anthropic-agent-skills`, `claude-code-plugins`,
  `claude-plugins-official`, `caveman`.
- **Habilitar** um plugin custa token em toda sessão (nome e descrição de cada
  skill entram no índice) e pode rodar hooks (`SessionStart`, `UserPromptSubmit`)
  na máquina. Por isso `enabledPlugins` está vazio.

Para usar algo daqui:

```bash
# marketplace ainda não registrado
/plugin marketplace add <owner>/<repo>
# habilitar o plugin
/plugin install <plugin>@<marketplace>
```

Antes de habilitar, olhe o `.claude-plugin/plugin.json` do repositório: se tiver
bloco `hooks`, algo vai executar na sua máquina a cada sessão.


## Marketplaces catalogados

| # | Repositório | Marketplace | Plugins |
|---|---|---|---|
| 1 | [obra/superpowers](https://github.com/obra/superpowers) | `superpowers-dev` | 1 |
| 2 | [mattpocock/skills](https://github.com/mattpocock/skills) | `mattpocock` | 1 |
| 3 | [affaan-m/ECC](https://github.com/affaan-m/ECC) | `ecc` | 1 |
| 4 | [multica-ai/andrej-karpathy-skills](https://github.com/multica-ai/andrej-karpathy-skills) | `karpathy-skills` | 1 |
| 5 | [anthropics/skills](https://github.com/anthropics/skills) | `anthropic-agent-skills` | 5 |
| 6 | [f/prompts.chat](https://github.com/f/prompts.chat) | `prompts.chat` | 1 |
| 7 | [anthropics/claude-code](https://github.com/anthropics/claude-code) | `claude-code-plugins` | 13 |
| 8 | [vercel/next.js](https://github.com/vercel/next.js) | `nextjs` | 1 |
| 9 | [DietrichGebert/ponytail](https://github.com/DietrichGebert/ponytail) | `ponytail` | 1 |
| 10 | [nextlevelbuilder/ui-ux-pro-max-skill](https://github.com/nextlevelbuilder/ui-ux-pro-max-skill) | `ui-ux-pro-max-skill` | 1 |
| 11 | [JuliusBrussee/caveman](https://github.com/JuliusBrussee/caveman) | `caveman` | 1 |
| 12 | [nexu-io/open-design](https://github.com/nexu-io/open-design) | `open-design` | 1 |
| 13 | [thedotmack/claude-mem](https://github.com/thedotmack/claude-mem) | `thedotmack` | 2 |
| 14 | [addyosmani/agent-skills](https://github.com/addyosmani/agent-skills) | `addy-agent-skills` | 1 |
| 15 | [ruvnet/RuView](https://github.com/ruvnet/RuView) | `ruview` | 1 |
| 16 | [storybookjs/storybook](https://github.com/storybookjs/storybook) | `storybook` | 1 |
| 17 | [Leonxlnx/taste-skill](https://github.com/Leonxlnx/taste-skill) | `taste-skill` | 1 |
| 18 | [Egonex-AI/Understand-Anything](https://github.com/Egonex-AI/Understand-Anything) | `understand-anything` | 1 |
| 19 | [ruvnet/ruflo](https://github.com/ruvnet/ruflo) | `ruflo` | 39 |
| 20 | [headroomlabs-ai/headroom](https://github.com/headroomlabs-ai/headroom) | `headroom-marketplace` | 1 |
| 21 | [career-ops-hq/career-ops](https://github.com/career-ops-hq/career-ops) | `career-ops` | 1 |
| 23 | [pbakaus/impeccable](https://github.com/pbakaus/impeccable) | `impeccable` | 1 |
| 24 | [mem0ai/mem0](https://github.com/mem0ai/mem0) | `mem0-plugins` | 1 |
| 25 | [upstash/context7](https://github.com/upstash/context7) | `context7-marketplace` | 1 |
| 26 | [mvanhorn/last30days-skill](https://github.com/mvanhorn/last30days-skill) | `last30days-skill` | 1 |
| 27 | [tw93/Pake](https://github.com/tw93/Pake) | `pake` | 1 |
| 28 | [MemPalace/mempalace](https://github.com/MemPalace/mempalace) | `mempalace` | 1 |
| 30 | [hugohe3/ppt-master](https://github.com/hugohe3/ppt-master) | `ppt-master` | 1 |
| 31 | [ChromeDevTools/chrome-devtools-mcp](https://github.com/ChromeDevTools/chrome-devtools-mcp) | `chrome-devtools-plugins` | 1 |
| 32 | [apple/container](https://github.com/apple/container) | `apple-container` | 1 |
| 33 | [coreyhaines31/marketingskills](https://github.com/coreyhaines31/marketingskills) | `marketingskills` | 1 |
| 34 | [HKUDS/CLI-Anything](https://github.com/HKUDS/CLI-Anything) | `cli-anything` | 1 |
| 35 | [heygen-com/hyperframes](https://github.com/heygen-com/hyperframes) | `hyperframes` | 2 |
| 36 | [slidevjs/slidev](https://github.com/slidevjs/slidev) | `slidev-plugins` | 1 |
| 37 | [kepano/obsidian-skills](https://github.com/kepano/obsidian-skills) | `obsidian-skills` | 1 |
| 38 | [Imbad0202/academic-research-skills](https://github.com/Imbad0202/academic-research-skills) | `academic-research-skills` | 1 |
| 39 | [abhigyanpatwari/GitNexus](https://github.com/abhigyanpatwari/GitNexus) | `gitnexus-marketplace` | 1 |
| 40 | [blader/humanizer](https://github.com/blader/humanizer) | `humanizer` | 1 |
| 41 | [sickn33/agentic-awesome-skills](https://github.com/sickn33/agentic-awesome-skills) | `agentic-awesome-skills` | 59 |
| 43 | [payloadcms/payload](https://github.com/payloadcms/payload) | `payload-marketplace` | 1 |
| 44 | [ccxt/ccxt](https://github.com/ccxt/ccxt) | `ccxt` | 1 |
| 45 | [ayghri/i-have-adhd](https://github.com/ayghri/i-have-adhd) | `i-have-adhd` | 1 |
| 47 | [vercel-labs/agent-browser](https://github.com/vercel-labs/agent-browser) | `agent-browser` | 1 |
| 48 | [saadeghi/daisyui](https://github.com/saadeghi/daisyui) | `daisyui` | 2 |
| 50 | [wshobson/agents](https://github.com/wshobson/agents) | `claude-code-workflows` | 94 |
| 51 | [Yeachan-Heo/oh-my-claudecode](https://github.com/Yeachan-Heo/oh-my-claudecode) | `omc` | 1 |
| 52 | [cathrynlavery/diagram-design](https://github.com/cathrynlavery/diagram-design) | `diagram-design` | 1 |
| 53 | [CopilotKit/CopilotKit](https://github.com/CopilotKit/CopilotKit) | `copilotkit-plugins` | 1 |
| 54 | [volcengine/OpenViking](https://github.com/volcengine/OpenViking) | `openviking` | 1 |
| 55 | [anthropics/claude-plugins-official](https://github.com/anthropics/claude-plugins-official) | `claude-plugins-official` | 308 |
| 56 | [anthropics/financial-services](https://github.com/anthropics/financial-services) | `claude-for-financial-services` | 19 |
| 57 | [huggingface/diffusers](https://github.com/huggingface/diffusers) | `diffusers-skills` | 1 |
| 58 | [openai/codex-plugin-cc](https://github.com/openai/codex-plugin-cc) | `openai-codex` | 1 |
| 59 | [mukul975/Anthropic-Cybersecurity-Skills](https://github.com/mukul975/Anthropic-Cybersecurity-Skills) | `anthropic-cybersecurity-skills` | 1 |
| 60 | [freestylefly/awesome-gpt-image-2](https://github.com/freestylefly/awesome-gpt-image-2) | `awesome-gpt-image-2` | 1 |
| 61 | [garrytan/gbrain](https://github.com/garrytan/gbrain) | `gbrain` | 3 |
| 62 | [tobi/qmd](https://github.com/tobi/qmd) | `qmd` | 1 |
| 63 | [zarazhangrui/frontend-slides](https://github.com/zarazhangrui/frontend-slides) | `frontend-slides` | 1 |
| 64 | [rohitg00/agentmemory](https://github.com/rohitg00/agentmemory) | `agentmemory` | 1 |
| 65 | [yamadashy/repomix](https://github.com/yamadashy/repomix) | `repomix` | 3 |
| 66 | [eyaltoledano/claude-task-master](https://github.com/eyaltoledano/claude-task-master) | `taskmaster` | 1 |
| 67 | [jarrodwatts/claude-hud](https://github.com/jarrodwatts/claude-hud) | `claude-hud` | 1 |
| 68 | [mlflow/mlflow](https://github.com/mlflow/mlflow) | `mlflow-plugins` | 1 |
| 69 | [gastownhall/beads](https://github.com/gastownhall/beads) | `beads-marketplace` | 1 |
| 70 | [OthmanAdi/planning-with-files](https://github.com/OthmanAdi/planning-with-files) | `planning-with-files` | 1 |
| 71 | [phuryn/pm-skills](https://github.com/phuryn/pm-skills) | `pm-skills` | 9 |
| 72 | [alirezarezvani/claude-skills](https://github.com/alirezarezvani/claude-skills) | `claude-code-skills` | 99 |
| 73 | [JimLiu/baoyu-skills](https://github.com/JimLiu/baoyu-skills) | `baoyu-skills` | 1 |
| 74 | [clockworklabs/SpacetimeDB](https://github.com/clockworklabs/SpacetimeDB) | `spacetimedb-plugins` | 1 |
| 75 | [promptfoo/promptfoo](https://github.com/promptfoo/promptfoo) | `promptfoo` | 1 |
| 76 | [EveryInc/compound-engineering-plugin](https://github.com/EveryInc/compound-engineering-plugin) | `compound-engineering-plugin` | 1 |
| 77 | [VoltAgent/awesome-claude-code-subagents](https://github.com/VoltAgent/awesome-claude-code-subagents) | `voltagent-subagents` | 10 |
| 78 | [anthropics/knowledge-work-plugins](https://github.com/anthropics/knowledge-work-plugins) | `knowledge-work-plugins` | 113 |
| 79 | [pascalorg/editor](https://github.com/pascalorg/editor) | `pascal` | 1 |
| 80 | [vectorize-io/hindsight](https://github.com/vectorize-io/hindsight) | `hindsight` | 2 |
| 81 | [alibaba/open-code-review](https://github.com/alibaba/open-code-review) | `open-code-review` | 1 |
| 82 | [mksglu/context-mode](https://github.com/mksglu/context-mode) | `context-mode` | 1 |
| 83 | [guillaumemeyer/watermarks-remover](https://github.com/guillaumemeyer/watermarks-remover) | `watermarks-remover` | 1 |
| 84 | [snarktank/ralph](https://github.com/snarktank/ralph) | `ralph-marketplace` | 1 |
| 85 | [dailydotdev/daily](https://github.com/dailydotdev/daily) | `daily.dev` | 2 |
| 87 | [google/skills](https://github.com/google/skills) | `google-plugins` | 17 |
| 88 | [tanweai/pua](https://github.com/tanweai/pua) | `pua-skills` | 1 |
| 89 | [every-app/open-seo](https://github.com/every-app/open-seo) | `openseo` | 1 |
| 90 | [confident-ai/deepeval](https://github.com/confident-ai/deepeval) | `deepeval-plugins` | 1 |
| 91 | [muratcankoylan/Agent-Skills-for-Context-Engineering](https://github.com/muratcankoylan/Agent-Skills-for-Context-Engineering) | `context-engineering-marketplace` | 1 |
| 92 | [browser-use/browser-harness](https://github.com/browser-use/browser-harness) | `browser-harness` | 1 |
| 93 | [bradautomates/claude-video](https://github.com/bradautomates/claude-video) | `claude-video` | 1 |
| 94 | [AgriciDaniel/claude-seo](https://github.com/AgriciDaniel/claude-seo) | `agricidaniel-claude-seo` | 1 |
| 95 | [ag-ui-protocol/ag-ui](https://github.com/ag-ui-protocol/ag-ui) | `ag-ui` | 1 |
| 96 | [citrolabs/ego-lite](https://github.com/citrolabs/ego-lite) | `ego-agent-skills` | 1 |
| 97 | [pipecat-ai/pipecat](https://github.com/pipecat-ai/pipecat) | `pipecat-dev-skills` | 1 |
| 98 | [earthtojake/text-to-cad](https://github.com/earthtojake/text-to-cad) | `text-to-cad` | 1 |
| 99 | [greensock/gsap-skills](https://github.com/greensock/gsap-skills) | `gsap-skills` | 1 |
| 100 | [AgriciDaniel/claude-obsidian](https://github.com/AgriciDaniel/claude-obsidian) | `agricidaniel-claude-obsidian` | 1 |
| — | [obra/superpowers-marketplace](https://github.com/obra/superpowers-marketplace) | `superpowers-marketplace` | 10 |

## Não registrados (colisão de nome)

Dois repositórios publicam o mesmo nome de marketplace e o Claude Code aceita só um.
Ficou catalogado o mais bem colocado na lista; para usar o outro, registre-o com
outro nome.

| Repositório | Nome em conflito | Mantido |
|---|---|---|
| [santifer/career-ops](https://github.com/santifer/career-ops) | `career-ops` | career-ops-hq/career-ops |
| [Lum1104/Understand-Anything](https://github.com/Lum1104/Understand-Anything) | `understand-anything` | Egonex-AI/Understand-Anything |
| [chopratejas/headroom](https://github.com/chopratejas/headroom) | `headroom-marketplace` | headroomlabs-ai/headroom |
| [sickn33/antigravity-awesome-skills](https://github.com/sickn33/antigravity-awesome-skills) | `agentic-awesome-skills` | sickn33/agentic-awesome-skills |
| [milla-jovovich/mempalace](https://github.com/milla-jovovich/mempalace) | `mempalace` | MemPalace/mempalace |
| [steveyegge/beads](https://github.com/steveyegge/beads) | `beads-marketplace` | gastownhall/beads |

## Plugins por marketplace

Identificador completo para usar em `/plugin install` ou em `enabledPlugins`.

<details><summary><code>superpowers-dev</code> — obra/superpowers (1)</summary>

- `superpowers@superpowers-dev`

</details>

<details><summary><code>mattpocock</code> — mattpocock/skills (1)</summary>

- `mattpocock-skills@mattpocock`

</details>

<details><summary><code>ecc</code> — affaan-m/ECC (1)</summary>

- `ecc@ecc`

</details>

<details><summary><code>karpathy-skills</code> — multica-ai/andrej-karpathy-skills (1)</summary>

- `andrej-karpathy-skills@karpathy-skills`

</details>

<details><summary><code>anthropic-agent-skills</code> — anthropics/skills (5)</summary>

- `document-skills@anthropic-agent-skills`
- `example-skills@anthropic-agent-skills`
- `claude-api@anthropic-agent-skills`
- `academy-guide@anthropic-agent-skills`
- `discernment-nudge@anthropic-agent-skills`

</details>

<details><summary><code>prompts.chat</code> — f/prompts.chat (1)</summary>

- `prompts.chat@prompts.chat`

</details>

<details><summary><code>claude-code-plugins</code> — anthropics/claude-code (13)</summary>

- `agent-sdk-dev@claude-code-plugins`
- `claude-opus-4-5-migration@claude-code-plugins`
- `code-review@claude-code-plugins`
- `commit-commands@claude-code-plugins`
- `explanatory-output-style@claude-code-plugins`
- `feature-dev@claude-code-plugins`
- `frontend-design@claude-code-plugins`
- `hookify@claude-code-plugins`
- `learning-output-style@claude-code-plugins`
- `plugin-dev@claude-code-plugins`
- `pr-review-toolkit@claude-code-plugins`
- `ralph-wiggum@claude-code-plugins`
- `security-guidance@claude-code-plugins`

</details>

<details><summary><code>nextjs</code> — vercel/next.js (1)</summary>

- `nextjs@nextjs`

</details>

<details><summary><code>ponytail</code> — DietrichGebert/ponytail (1)</summary>

- `ponytail@ponytail`

</details>

<details><summary><code>ui-ux-pro-max-skill</code> — nextlevelbuilder/ui-ux-pro-max-skill (1)</summary>

- `ui-ux-pro-max@ui-ux-pro-max-skill`

</details>

<details><summary><code>caveman</code> — JuliusBrussee/caveman (1)</summary>

- `caveman@caveman`

</details>

<details><summary><code>open-design</code> — nexu-io/open-design (1)</summary>

- `open-design@open-design`

</details>

<details><summary><code>thedotmack</code> — thedotmack/claude-mem (2)</summary>

- `claude-mem@thedotmack`
- `claude-mem-cowork@thedotmack`

</details>

<details><summary><code>addy-agent-skills</code> — addyosmani/agent-skills (1)</summary>

- `agent-skills@addy-agent-skills`

</details>

<details><summary><code>ruview</code> — ruvnet/RuView (1)</summary>

- `ruview@ruview`

</details>

<details><summary><code>storybook</code> — storybookjs/storybook (1)</summary>

- `storybook@storybook`

</details>

<details><summary><code>taste-skill</code> — Leonxlnx/taste-skill (1)</summary>

- `taste-skill@taste-skill`

</details>

<details><summary><code>understand-anything</code> — Egonex-AI/Understand-Anything (1)</summary>

- `understand-anything@understand-anything`

</details>

<details><summary><code>ruflo</code> — ruvnet/ruflo (39)</summary>

- `ruflo-core@ruflo`
- `ruflo-swarm@ruflo`
- `ruflo-loop-workers@ruflo`
- `ruflo-security-audit@ruflo`
- `ruflo-rag-memory@ruflo`
- `ruflo-testgen@ruflo`
- `ruflo-docs@ruflo`
- `ruflo-autopilot@ruflo`
- `ruflo-intelligence@ruflo`
- `ruflo-agentdb@ruflo`
- `ruflo-aidefence@ruflo`
- `ruflo-browser@ruflo`
- `ruflo-jujutsu@ruflo`
- `ruflo-agent@ruflo`
- `ruflo-workflows@ruflo`
- `ruflo-daa@ruflo`
- `ruflo-ruvllm@ruflo`
- `ruflo-rvf@ruflo`
- `ruflo-plugin-creator@ruflo`
- `ruflo-goals@ruflo`
- `ruflo-adr@ruflo`
- `ruflo-cost-tracker@ruflo`
- `ruflo-ddd@ruflo`
- `ruflo-federation@ruflo`
- `ruflo-graph-intelligence@ruflo`
- `ruflo-iot-cognitum@ruflo`
- `ruflo-knowledge-graph@ruflo`
- `ruflo-market-data@ruflo`
- `ruflo-migrations@ruflo`
- `ruflo-neural-trader@ruflo`
- `ruflo-observability@ruflo`
- `ruflo-ruvector@ruflo`
- `ruflo-sparc@ruflo`
- `ruflo-metaharness@ruflo`
- `ruflo-arena@ruflo`
- `ruflo-agntcy@ruflo`
- `ruflo-bbs-federation@ruflo`
- `ruflo-business-pods@ruflo`
- `ruflo-music@ruflo`

</details>

<details><summary><code>headroom-marketplace</code> — headroomlabs-ai/headroom (1)</summary>

- `headroom@headroom-marketplace`

</details>

<details><summary><code>career-ops</code> — career-ops-hq/career-ops (1)</summary>

- `career-ops@career-ops`

</details>

<details><summary><code>impeccable</code> — pbakaus/impeccable (1)</summary>

- `impeccable@impeccable`

</details>

<details><summary><code>mem0-plugins</code> — mem0ai/mem0 (1)</summary>

- `mem0@mem0-plugins`

</details>

<details><summary><code>context7-marketplace</code> — upstash/context7 (1)</summary>

- `context7@context7-marketplace`

</details>

<details><summary><code>last30days-skill</code> — mvanhorn/last30days-skill (1)</summary>

- `last30days@last30days-skill`

</details>

<details><summary><code>pake</code> — tw93/Pake (1)</summary>

- `pake@pake`

</details>

<details><summary><code>mempalace</code> — MemPalace/mempalace (1)</summary>

- `mempalace@mempalace`

</details>

<details><summary><code>ppt-master</code> — hugohe3/ppt-master (1)</summary>

- `ppt-master@ppt-master`

</details>

<details><summary><code>chrome-devtools-plugins</code> — ChromeDevTools/chrome-devtools-mcp (1)</summary>

- `chrome-devtools-mcp@chrome-devtools-plugins`

</details>

<details><summary><code>apple-container</code> — apple/container (1)</summary>

- `container@apple-container`

</details>

<details><summary><code>marketingskills</code> — coreyhaines31/marketingskills (1)</summary>

- `marketing-skills@marketingskills`

</details>

<details><summary><code>cli-anything</code> — HKUDS/CLI-Anything (1)</summary>

- `cli-anything@cli-anything`

</details>

<details><summary><code>hyperframes</code> — heygen-com/hyperframes (2)</summary>

- `core-skills@hyperframes`
- `hyperframes@hyperframes`

</details>

<details><summary><code>slidev-plugins</code> — slidevjs/slidev (1)</summary>

- `slidev@slidev-plugins`

</details>

<details><summary><code>obsidian-skills</code> — kepano/obsidian-skills (1)</summary>

- `obsidian@obsidian-skills`

</details>

<details><summary><code>academic-research-skills</code> — Imbad0202/academic-research-skills (1)</summary>

- `academic-research-skills@academic-research-skills`

</details>

<details><summary><code>gitnexus-marketplace</code> — abhigyanpatwari/GitNexus (1)</summary>

- `gitnexus@gitnexus-marketplace`

</details>

<details><summary><code>humanizer</code> — blader/humanizer (1)</summary>

- `humanizer@humanizer`

</details>

<details><summary><code>agentic-awesome-skills</code> — sickn33/agentic-awesome-skills (59)</summary>

- `agentic-awesome-skills@agentic-awesome-skills`
- `agentic-bundle-essentials@agentic-awesome-skills`
- `agentic-bundle-security-engineer@agentic-awesome-skills`
- `agentic-bundle-security-developer@agentic-awesome-skills`
- `agentic-bundle-web-wizard@agentic-awesome-skills`
- `agentic-bundle-web-designer@agentic-awesome-skills`
- `agentic-bundle-full-stack-developer@agentic-awesome-skills`
- `agentic-bundle-agent-architect@agentic-awesome-skills`
- `agentic-bundle-llm-application-developer@agentic-awesome-skills`
- `agentic-bundle-indie-game-dev@agentic-awesome-skills`
- `agentic-bundle-python-pro@agentic-awesome-skills`
- `agentic-bundle-typescript-javascript@agentic-awesome-skills`
- `agentic-bundle-systems-programming@agentic-awesome-skills`
- `agentic-bundle-startup-founder@agentic-awesome-skills`
- `agentic-bundle-business-analyst@agentic-awesome-skills`
- `agentic-bundle-marketing-growth@agentic-awesome-skills`
- `agentic-bundle-devops-cloud@agentic-awesome-skills`
- `agentic-bundle-observability-monitoring@agentic-awesome-skills`
- `agentic-bundle-data-analytics@agentic-awesome-skills`
- `agentic-bundle-data-engineering@agentic-awesome-skills`
- `agentic-bundle-creative-director@agentic-awesome-skills`
- `agentic-bundle-qa-testing@agentic-awesome-skills`
- `agentic-bundle-aas-web-app-builder@agentic-awesome-skills`
- `agentic-bundle-aas-product-design-studio@agentic-awesome-skills`
- `agentic-bundle-aas-security-engineer@agentic-awesome-skills`
- `agentic-bundle-aas-secure-app-builder@agentic-awesome-skills`
- `agentic-bundle-aas-documents-presentations@agentic-awesome-skills`
- `agentic-bundle-aas-data-analytics@agentic-awesome-skills`
- `agentic-bundle-aas-agent-mcp-builder@agentic-awesome-skills`
- `agentic-bundle-aas-qa-test-automation@agentic-awesome-skills`
- `agentic-bundle-aas-devops-cloud@agentic-awesome-skills`
- `agentic-bundle-aas-marketing-seo-growth@agentic-awesome-skills`
- `agentic-bundle-aas-automation-builder@agentic-awesome-skills`
- `agentic-bundle-aas-observability-ir@agentic-awesome-skills`
- `agentic-bundle-aas-python-api-builder@agentic-awesome-skills`
- `agentic-bundle-aas-mobile-app-builder@agentic-awesome-skills`
- `agentic-bundle-mobile-developer@agentic-awesome-skills`
- `agentic-bundle-integration-apis@agentic-awesome-skills`
- `agentic-bundle-architecture-design@agentic-awesome-skills`
- `agentic-bundle-ddd-evented-architecture@agentic-awesome-skills`
- `agentic-bundle-automation-builder@agentic-awesome-skills`
- `agentic-bundle-revops-crm-automation@agentic-awesome-skills`
- `agentic-bundle-commerce-payments@agentic-awesome-skills`
- `agentic-bundle-odoo-erp@agentic-awesome-skills`
- `agentic-bundle-azure-ai-cloud@agentic-awesome-skills`
- `agentic-bundle-expo-react-native@agentic-awesome-skills`
- `agentic-bundle-apple-platform-design@agentic-awesome-skills`
- `agentic-bundle-makepad-builder@agentic-awesome-skills`
- `agentic-bundle-seo-specialist@agentic-awesome-skills`
- `agentic-bundle-documents-presentations@agentic-awesome-skills`
- `agentic-bundle-oss-maintainer@agentic-awesome-skills`
- `agentic-bundle-skill-author@agentic-awesome-skills`
- `agentic-bundle-aas-accessibility-inclusive-ux@agentic-awesome-skills`
- `agentic-bundle-aas-api-platform-builder@agentic-awesome-skills`
- `agentic-bundle-aas-saas-launch-revenue@agentic-awesome-skills`
- `agentic-bundle-aas-ai-product-evaluation-ops@agentic-awesome-skills`
- `agentic-bundle-aas-data-engineering-platform@agentic-awesome-skills`
- `agentic-bundle-aas-privacy-compliance-engineering@agentic-awesome-skills`
- `agentic-bundle-aas-localization-international-growth@agentic-awesome-skills`

</details>

<details><summary><code>payload-marketplace</code> — payloadcms/payload (1)</summary>

- `payload@payload-marketplace`

</details>

<details><summary><code>ccxt</code> — ccxt/ccxt (1)</summary>

- `ccxt-mcp@ccxt`

</details>

<details><summary><code>i-have-adhd</code> — ayghri/i-have-adhd (1)</summary>

- `i-have-adhd@i-have-adhd`

</details>

<details><summary><code>agent-browser</code> — vercel-labs/agent-browser (1)</summary>

- `agent-browser@agent-browser`

</details>

<details><summary><code>daisyui</code> — saadeghi/daisyui (2)</summary>

- `daisyui@daisyui`
- `daisyui-blueprint@daisyui`

</details>

<details><summary><code>claude-code-workflows</code> — wshobson/agents (94)</summary>

- `documentation-standards@claude-code-workflows`
- `code-documentation@claude-code-workflows`
- `debugging-toolkit@claude-code-workflows`
- `git-pr-workflows@claude-code-workflows`
- `operating-kit@claude-code-workflows`
- `backend-development@claude-code-workflows`
- `frontend-mobile-development@claude-code-workflows`
- `full-stack-orchestration@claude-code-workflows`
- `unit-testing@claude-code-workflows`
- `tdd-workflows@claude-code-workflows`
- `code-refactoring@claude-code-workflows`
- `dependency-management@claude-code-workflows`
- `error-debugging@claude-code-workflows`
- `team-collaboration@claude-code-workflows`
- `llm-application-dev@claude-code-workflows`
- `llm-finetuning@claude-code-workflows`
- `agent-orchestration@claude-code-workflows`
- `context-management@claude-code-workflows`
- `machine-learning-ops@claude-code-workflows`
- `data-engineering@claude-code-workflows`
- `incident-response@claude-code-workflows`
- `error-diagnostics@claude-code-workflows`
- `distributed-debugging@claude-code-workflows`
- `observability-monitoring@claude-code-workflows`
- `deployment-strategies@claude-code-workflows`
- `deployment-validation@claude-code-workflows`
- `kubernetes-operations@claude-code-workflows`
- `cloud-infrastructure@claude-code-workflows`
- `cicd-automation@claude-code-workflows`
- `application-performance@claude-code-workflows`
- `database-cloud-optimization@claude-code-workflows`
- `comprehensive-review@claude-code-workflows`
- `performance-testing-review@claude-code-workflows`
- `framework-migration@claude-code-workflows`
- `codebase-cleanup@claude-code-workflows`
- `database-design@claude-code-workflows`
- `database-migrations@claude-code-workflows`
- `security-scanning@claude-code-workflows`
- `security-compliance@claude-code-workflows`
- `backend-api-security@claude-code-workflows`
- `frontend-mobile-security@claude-code-workflows`
- `data-validation-suite@claude-code-workflows`
- `api-scaffolding@claude-code-workflows`
- `api-testing-observability@claude-code-workflows`
- `seo-content-creation@claude-code-workflows`
- `seo-technical-optimization@claude-code-workflows`
- `seo-analysis-monitoring@claude-code-workflows`
- `documentation-generation@claude-code-workflows`
- `c4-architecture@claude-code-workflows`
- `avoid-ai-writing@claude-code-workflows`
- `multi-platform-apps@claude-code-workflows`
- `business-analytics@claude-code-workflows`
- `startup-business-analyst@claude-code-workflows`
- `before-you-build@claude-code-workflows`
- `hr-legal-compliance@claude-code-workflows`
- `customer-sales-automation@claude-code-workflows`
- `content-marketing@claude-code-workflows`
- `social-publishing@claude-code-workflows`
- `hermes-tweet@claude-code-workflows`
- `blockchain-web3@claude-code-workflows`
- `quantitative-trading@claude-code-workflows`
- `payment-processing@claude-code-workflows`
- `game-development@claude-code-workflows`
- `accessibility-compliance@claude-code-workflows`
- `python-development@claude-code-workflows`
- `javascript-typescript@claude-code-workflows`
- `systems-programming@claude-code-workflows`
- `jvm-languages@claude-code-workflows`
- `web-scripting@claude-code-workflows`
- `functional-programming@claude-code-workflows`
- `julia-development@claude-code-workflows`
- `arm-cortex-microcontrollers@claude-code-workflows`
- `shell-scripting@claude-code-workflows`
- `developer-essentials@claude-code-workflows`
- `dgx-spark-ops@claude-code-workflows`
- `reverse-engineering@claude-code-workflows`
- `conductor@claude-code-workflows`
- `superself@claude-code-workflows`
- `ui-design@claude-code-workflows`
- `agent-teams@claude-code-workflows`
- `dotnet-contribution@claude-code-workflows`
- `meigen-ai-design@claude-code-workflows`
- `brand-landingpage@claude-code-workflows`
- `plugin-eval@claude-code-workflows`
- `block-no-verify@claude-code-workflows`
- `pensyve@claude-code-workflows`
- `hol-guard@claude-code-workflows`
- `protect-mcp@claude-code-workflows`
- `signed-audit-trails@claude-code-workflows`
- `review-agent-governance@claude-code-workflows`
- `ship-mate@claude-code-workflows`
- `file-conversion@claude-code-workflows`
- `skill-forge-essentials@claude-code-workflows`
- `pptx-deck-creation@claude-code-workflows`

</details>

<details><summary><code>omc</code> — Yeachan-Heo/oh-my-claudecode (1)</summary>

- `oh-my-claudecode@omc`

</details>

<details><summary><code>diagram-design</code> — cathrynlavery/diagram-design (1)</summary>

- `diagram-design@diagram-design`

</details>

<details><summary><code>copilotkit-plugins</code> — CopilotKit/CopilotKit (1)</summary>

- `copilotkit@copilotkit-plugins`

</details>

<details><summary><code>openviking</code> — volcengine/OpenViking (1)</summary>

- `openviking-memory@openviking`

</details>

<details><summary><code>claude-plugins-official</code> — anthropics/claude-plugins-official (308)</summary>

- `42crunch-api-security-testing@claude-plugins-official`
- `adobe-for-creativity@claude-plugins-official`
- `agent-sdk-dev@claude-plugins-official`
- `agentforce-adlc@claude-plugins-official`
- `ai-plugins@claude-plugins-official`
- `aikido@claude-plugins-official`
- `airtable@claude-plugins-official`
- `airwallex-agentos@claude-plugins-official`
- `airwallex-dev@claude-plugins-official`
- `aiven@claude-plugins-official`
- `alloydb@claude-plugins-official`
- `alloydb-omni@claude-plugins-official`
- `altimate-code@claude-plugins-official`
- `amazon-location-service@claude-plugins-official`
- `amd-skills@claude-plugins-official`
- `amplitude@claude-plugins-official`
- `apollo@claude-plugins-official`
- `apollo-skills@claude-plugins-official`
- `appwrite@claude-plugins-official`
- `asana@claude-plugins-official`
- `astronomer-data-agents@claude-plugins-official`
- `atlan@claude-plugins-official`
- `atlassian@claude-plugins-official`
- `atlassian-twg-cli@claude-plugins-official`
- `atomic-agents@claude-plugins-official`
- `auth0@claude-plugins-official`
- `aws-agents@claude-plugins-official`
- `aws-agents-for-devsecops@claude-plugins-official`
- `aws-amplify@claude-plugins-official`
- `aws-core@claude-plugins-official`
- `aws-data-analytics@claude-plugins-official`
- `aws-serverless@claude-plugins-official`
- `aws-startup-advisor@claude-plugins-official`
- `aws-transform@claude-plugins-official`
- `azure@claude-plugins-official`
- `azure-cosmos-db-assistant@claude-plugins-official`
- `azure-sql-developer@claude-plugins-official`
- `base44@claude-plugins-official`
- `bigdata-com@claude-plugins-official`
- `bigquery-data-analytics@claude-plugins-official`
- `boltz@claude-plugins-official`
- `blackrock-advisor-center-plugin@claude-plugins-official`
- `box@claude-plugins-official`
- `brightdata-plugin@claude-plugins-official`
- `browser-use@claude-plugins-official`
- `buildkite@claude-plugins-official`
- `canva@claude-plugins-official`
- `carbone-skill@claude-plugins-official`
- `carta-cap-table@claude-plugins-official`
- `carta-crm@claude-plugins-official`
- `carta-investors@claude-plugins-official`
- `catalyst-by-zoho@claude-plugins-official`
- `cds-mcp@claude-plugins-official`
- `chrome-devtools-mcp@claude-plugins-official`
- `chronograph-gp@claude-plugins-official`
- `chronograph-lp@claude-plugins-official`
- `circle-skills@claude-plugins-official`
- `circleback@claude-plugins-official`
- `ckeditor@claude-plugins-official`
- `clangd-lsp@claude-plugins-official`
- `claude-code-setup@claude-plugins-official`
- `claude-md-management@claude-plugins-official`
- `claude-security@claude-plugins-official`
- `clay@claude-plugins-official`
- `clickhouse@claude-plugins-official`
- `clickhouse-best-practices@claude-plugins-official`
- `cloud-sql-mysql@claude-plugins-official`
- `cloud-sql-postgresql@claude-plugins-official`
- `cloud-sql-sqlserver@claude-plugins-official`
- `cloudflare@claude-plugins-official`
- `cloudinary@claude-plugins-official`
- `cockroachdb@claude-plugins-official`
- `code-modernization@claude-plugins-official`
- `code-review@claude-plugins-official`
- `code-simplifier@claude-plugins-official`
- `coderabbit@claude-plugins-official`
- `codspeed@claude-plugins-official`
- `commit-commands@claude-plugins-official`
- `confidence@claude-plugins-official`
- `context7@claude-plugins-official`
- `convex@claude-plugins-official`
- `crowdsec@claude-plugins-official`
- `crowdstrike-falcon-foundry@claude-plugins-official`
- `crowdstrike-falcon-fusion@claude-plugins-official`
- `csharp-lsp@claude-plugins-official`
- `cwc-makers@claude-plugins-official`
- `dash0@claude-plugins-official`
- `data@claude-plugins-official`
- `data-agent-kit-starter-pack@claude-plugins-official`
- `data-engineering@claude-plugins-official`
- `databases-on-aws@claude-plugins-official`
- `databricks@claude-plugins-official`
- `datadog@claude-plugins-official`
- `datahub-skills@claude-plugins-official`
- `dataproc@claude-plugins-official`
- `datarobot-agent-skills@claude-plugins-official`
- `dataverse@claude-plugins-official`
- `deepeval@claude-plugins-official`
- `deploy-on-aws@claude-plugins-official`
- `desktop-commander@claude-plugins-official`
- `discord@claude-plugins-official`
- `dominodatalab@claude-plugins-official`
- `dropbox@claude-plugins-official`
- `duckdb-skills@claude-plugins-official`
- `duende-skills@claude-plugins-official`
- `exa@claude-plugins-official`
- `explanatory-output-style@claude-plugins-official`
- `expo@claude-plugins-official`
- `fakechat@claude-plugins-official`
- `fastly-agent-toolkit@claude-plugins-official`
- `feature-dev@claude-plugins-official`
- `fiftyone@claude-plugins-official`
- `figma@claude-plugins-official`
- `firebase@claude-plugins-official`
- `firecrawl@claude-plugins-official`
- `firestore-native@claude-plugins-official`
- `forge-skills@claude-plugins-official`
- `frontend-design@claude-plugins-official`
- `fullstory@claude-plugins-official`
- `gc-ai@claude-plugins-official`
- `github@claude-plugins-official`
- `gitkraken@claude-plugins-official`
- `gitlab@claude-plugins-official`
- `google-cloud-storage@claude-plugins-official`
- `gopls-lsp@claude-plugins-official`
- `grafana-assistant@claude-plugins-official`
- `grafana-cloud-mcp@claude-plugins-official`
- `grafana-mcp@claude-plugins-official`
- `greptile@claude-plugins-official`
- `growthbook@claude-plugins-official`
- `honeycomb@claude-plugins-official`
- `hookify@claude-plugins-official`
- `hostinger@claude-plugins-official`
- `huggingface-skills@claude-plugins-official`
- `hunter@claude-plugins-official`
- `hyperframes@claude-plugins-official`
- `idmp-plugin@claude-plugins-official`
- `imessage@claude-plugins-official`
- `informatica-for-claude-platform@claude-plugins-official`
- `intercom@claude-plugins-official`
- `intuit-quickbooks@claude-plugins-official`
- `jdtls-lsp@claude-plugins-official`
- `jfrog@claude-plugins-official`
- `knowledge-catalog@claude-plugins-official`
- `kotlin-lsp@claude-plugins-official`
- `langfuse-observability@claude-plugins-official`
- `laravel-boost@claude-plugins-official`
- `leadfeeder@claude-plugins-official`
- `learn-with-coursera@claude-plugins-official`
- `learning-output-style@claude-plugins-official`
- `legalzoom@claude-plugins-official`
- `linear@claude-plugins-official`
- `liquid-lsp@claude-plugins-official`
- `liquid-skills@claude-plugins-official`
- `logfire@claude-plugins-official`
- `logrocket@claude-plugins-official`
- `looker@claude-plugins-official`
- `lovable@claude-plugins-official`
- `lua-lsp@claude-plugins-official`
- `lumen@claude-plugins-official`
- `lusha@claude-plugins-official`
- `mapbox@claude-plugins-official`
- `math-olympiad@claude-plugins-official`
- `mattpocock-skills@claude-plugins-official`
- `mcp-apps@claude-plugins-official`
- `mcp-server-dev@claude-plugins-official`
- `mcp-tunnels@claude-plugins-official`
- `mercadopago@claude-plugins-official`
- `mergify@claude-plugins-official`
- `microsoft-docs@claude-plugins-official`
- `migration-to-aws@claude-plugins-official`
- `mintlify@claude-plugins-official`
- `miro@claude-plugins-official`
- `modern-web-guidance@claude-plugins-official`
- `mlflow@claude-plugins-official`
- `monday-crm@claude-plugins-official`
- `mongodb@claude-plugins-official`
- `mongodb-atlas@claude-plugins-official`
- `neon@claude-plugins-official`
- `netlify-skills@claude-plugins-official`
- `netsuite-ai-companion@claude-plugins-official`
- `netsuite-finance-analyst@claude-plugins-official`
- `netsuite-suitecloud@claude-plugins-official`
- `newrelic@claude-plugins-official`
- `nightvision@claude-plugins-official`
- `nimble@claude-plugins-official`
- `noibu@claude-plugins-official`
- `notion@claude-plugins-official`
- `nvidia-skills@claude-plugins-official`
- `oracle-ai-data-platform-workbench-databricks-migrator@claude-plugins-official`
- `oracle-ai-data-platform-workbench-engineer-agent@claude-plugins-official`
- `oracle-ai-data-platform-workbench-spark-connectors@claude-plugins-official`
- `oracledb@claude-plugins-official`
- `outputai@claude-plugins-official`
- `pagerduty@claude-plugins-official`
- `paypal@claude-plugins-official`
- `pendo-analytics@claude-plugins-official`
- `pendo-guides@claude-plugins-official`
- `pendo-orchestrate@claude-plugins-official`
- `php-lsp@claude-plugins-official`
- `pigment@claude-plugins-official`
- `pinecone@claude-plugins-official`
- `pixeltable@claude-plugins-official`
- `planetscale@claude-plugins-official`
- `playground@claude-plugins-official`
- `playwright@claude-plugins-official`
- `plugin-dev@claude-plugins-official`
- `posthog@claude-plugins-official`
- `postiz@claude-plugins-official`
- `postman@claude-plugins-official`
- `pr-review-toolkit@claude-plugins-official`
- `preset-cli-skills@claude-plugins-official`
- `prisma@claude-plugins-official`
- `project-artifact@claude-plugins-official`
- `pydantic-ai@claude-plugins-official`
- `pyright-lsp@claude-plugins-official`
- `qdrant-skills@claude-plugins-official`
- `qodo@claude-plugins-official`
- `qodo-standards@claude-plugins-official`
- `qt-development-skills@claude-plugins-official`
- `quarkus-agent@claude-plugins-official`
- `railway@claude-plugins-official`
- `ralph-loop@claude-plugins-official`
- `rc@claude-plugins-official`
- `receipts@claude-plugins-official`
- `redis-development@claude-plugins-official`
- `remember@claude-plugins-official`
- `render@claude-plugins-official`
- `resend@claude-plugins-official`
- `revenuecat@claude-plugins-official`
- `rill@claude-plugins-official`
- `rootly@claude-plugins-official`
- `ruby-lsp@claude-plugins-official`
- `runway-api@claude-plugins-official`
- `rust-analyzer-lsp@claude-plugins-official`
- `sagemaker-ai@claude-plugins-official`
- `salesforce-development@claude-plugins-official`
- `sanity@claude-plugins-official`
- `sap-cds-mcp@claude-plugins-official`
- `sap-fiori-mcp-server@claude-plugins-official`
- `sap-hana-cli@claude-plugins-official`
- `sap-mdk-server@claude-plugins-official`
- `save-to-spotify@claude-plugins-official`
- `scandit-sdk@claude-plugins-official`
- `security-guidance@claude-plugins-official`
- `semgrep@claude-plugins-official`
- `sentry@claude-plugins-official`
- `sentry-cli@claude-plugins-official`
- `serena@claude-plugins-official`
- `servicenow-sdk@claude-plugins-official`
- `session-report@claude-plugins-official`
- `setup-agent-analytics@claude-plugins-official`
- `setup-mcp-agent-analytics@claude-plugins-official`
- `shippo@claude-plugins-official`
- `shopify-ai-toolkit@claude-plugins-official`
- `skill-creator@claude-plugins-official`
- `slack@claude-plugins-official`
- `snowflake-cortex-code@claude-plugins-official`
- `sonarqube@claude-plugins-official`
- `sonatype-guide@claude-plugins-official`
- `sourcegraph@claude-plugins-official`
- `spanner@claude-plugins-official`
- `spotify-ads-api@claude-plugins-official`
- `stackhawk-hawkscan@claude-plugins-official`
- `stackhawk-api@claude-plugins-official`
- `streaming-skills-plugin@claude-plugins-official`
- `stripe@claude-plugins-official`
- `sumup@claude-plugins-official`
- `supabase@claude-plugins-official`
- `superdesign@claude-plugins-official`
- `superpowers@claude-plugins-official`
- `swift-lsp@claude-plugins-official`
- `synthflow@claude-plugins-official`
- `tavily@claude-plugins-official`
- `teamcity-cli@claude-plugins-official`
- `telegram@claude-plugins-official`
- `terraform@claude-plugins-official`
- `togetherai-skills@claude-plugins-official`
- `twilio-developer-kit@claude-plugins-official`
- `typescript-lsp@claude-plugins-official`
- `ui-theme-designer@claude-plugins-official`
- `ui5@claude-plugins-official`
- `ui5-modernization@claude-plugins-official`
- `ui5-typescript-conversion@claude-plugins-official`
- `unity@claude-plugins-official`
- `unreal-engine-skills-for-claude-code@claude-plugins-official`
- `valtown@claude-plugins-official`
- `vanta@claude-plugins-official`
- `vanta-mcp-plugin@claude-plugins-official`
- `vercel@claude-plugins-official`
- `vibe-prospecting@claude-plugins-official`
- `vsql-extension-builder@claude-plugins-official`
- `windsor-ai@claude-plugins-official`
- `wix@claude-plugins-official`
- `build-with-wordpress@claude-plugins-official`
- `workos@claude-plugins-official`
- `youdotcom-agent-skills@claude-plugins-official`
- `zapier@claude-plugins-official`
- `zilliz@claude-plugins-official`
- `zocks-advisor@claude-plugins-official`
- `zoom-plugin@claude-plugins-official`
- `zoominfo@claude-plugins-official`
- `zscaler@claude-plugins-official`
- `langfuse@claude-plugins-official`
- `zyte-web-data@claude-plugins-official`
- `activecampaign@claude-plugins-official`
- `hubspot-sales@claude-plugins-official`
- `dynatrace@claude-plugins-official`

</details>

<details><summary><code>claude-for-financial-services</code> — anthropics/financial-services (19)</summary>

- `financial-analysis@claude-for-financial-services`
- `investment-banking@claude-for-financial-services`
- `equity-research@claude-for-financial-services`
- `private-equity@claude-for-financial-services`
- `fund-admin@claude-for-financial-services`
- `operations@claude-for-financial-services`
- `pitch-agent@claude-for-financial-services`
- `market-researcher@claude-for-financial-services`
- `earnings-reviewer@claude-for-financial-services`
- `meeting-prep-agent@claude-for-financial-services`
- `model-builder@claude-for-financial-services`
- `gl-reconciler@claude-for-financial-services`
- `kyc-screener@claude-for-financial-services`
- `valuation-reviewer@claude-for-financial-services`
- `month-end-closer@claude-for-financial-services`
- `statement-auditor@claude-for-financial-services`
- `lseg@claude-for-financial-services`
- `sp-global@claude-for-financial-services`
- `claude-for-msft-365-install@claude-for-financial-services`

</details>

<details><summary><code>diffusers-skills</code> — huggingface/diffusers (1)</summary>

- `diffusers@diffusers-skills`

</details>

<details><summary><code>openai-codex</code> — openai/codex-plugin-cc (1)</summary>

- `codex@openai-codex`

</details>

<details><summary><code>anthropic-cybersecurity-skills</code> — mukul975/Anthropic-Cybersecurity-Skills (1)</summary>

- `cybersecurity-skills@anthropic-cybersecurity-skills`

</details>

<details><summary><code>awesome-gpt-image-2</code> — freestylefly/awesome-gpt-image-2 (1)</summary>

- `gpt-image-2-style-library@awesome-gpt-image-2`

</details>

<details><summary><code>gbrain</code> — garrytan/gbrain (3)</summary>

- `gbrain@gbrain`
- `gbrain-coding@gbrain`
- `gbrain-daily@gbrain`

</details>

<details><summary><code>qmd</code> — tobi/qmd (1)</summary>

- `qmd@qmd`

</details>

<details><summary><code>frontend-slides</code> — zarazhangrui/frontend-slides (1)</summary>

- `frontend-slides@frontend-slides`

</details>

<details><summary><code>agentmemory</code> — rohitg00/agentmemory (1)</summary>

- `agentmemory@agentmemory`

</details>

<details><summary><code>repomix</code> — yamadashy/repomix (3)</summary>

- `repomix-mcp@repomix`
- `repomix-commands@repomix`
- `repomix-explorer@repomix`

</details>

<details><summary><code>taskmaster</code> — eyaltoledano/claude-task-master (1)</summary>

- `taskmaster@taskmaster`

</details>

<details><summary><code>claude-hud</code> — jarrodwatts/claude-hud (1)</summary>

- `claude-hud@claude-hud`

</details>

<details><summary><code>mlflow-plugins</code> — mlflow/mlflow (1)</summary>

- `mlflow-tracing@mlflow-plugins`

</details>

<details><summary><code>beads-marketplace</code> — gastownhall/beads (1)</summary>

- `beads@beads-marketplace`

</details>

<details><summary><code>planning-with-files</code> — OthmanAdi/planning-with-files (1)</summary>

- `planning-with-files@planning-with-files`

</details>

<details><summary><code>pm-skills</code> — phuryn/pm-skills (9)</summary>

- `pm-product-discovery@pm-skills`
- `pm-product-strategy@pm-skills`
- `pm-execution@pm-skills`
- `pm-market-research@pm-skills`
- `pm-data-analytics@pm-skills`
- `pm-go-to-market@pm-skills`
- `pm-marketing-growth@pm-skills`
- `pm-toolkit@pm-skills`
- `pm-ai-shipping@pm-skills`

</details>

<details><summary><code>claude-code-skills</code> — alirezarezvani/claude-skills (99)</summary>

- `marketing-skills@claude-code-skills`
- `c-level-skills@claude-code-skills`
- `c-level-agents@claude-code-skills`
- `general-counsel-advisor@claude-code-skills`
- `arquiteto-de-empresa@claude-code-skills`
- `chief-data-officer-advisor@claude-code-skills`
- `vpe-advisor@claude-code-skills`
- `chief-customer-officer-advisor@claude-code-skills`
- `chief-ai-officer-advisor@claude-code-skills`
- `engineering-advanced-skills@claude-code-skills`
- `engineering-skills@claude-code-skills`
- `ra-qm-skills@claude-code-skills`
- `product-skills@claude-code-skills`
- `pm-skills@claude-code-skills`
- `business-growth-skills@claude-code-skills`
- `finance-skills@claude-code-skills`
- `pw@claude-code-skills`
- `self-improving-agent@claude-code-skills`
- `autoresearch-agent@claude-code-skills`
- `google-workspace-cli@claude-code-skills`
- `code-to-prd@claude-code-skills`
- `agenthub@claude-code-skills`
- `a11y-audit@claude-code-skills`
- `executive-mentor@claude-code-skills`
- `docker-development@claude-code-skills`
- `helm-chart-builder@claude-code-skills`
- `terraform-patterns@claude-code-skills`
- `research-summarizer@claude-code-skills`
- `code-tour@claude-code-skills`
- `demo-video@claude-code-skills`
- `data-quality-auditor@claude-code-skills`
- `statistical-analyst@claude-code-skills`
- `apple-hig-expert@claude-code-skills`
- `llm-wiki@claude-code-skills`
- `karpathy-coder@claude-code-skills`
- `feature-flags-architect@claude-code-skills`
- `kubernetes-operator@claude-code-skills`
- `chaos-engineering@claude-code-skills`
- `slo-architect@claude-code-skills`
- `write-a-skill@claude-code-skills`
- `book-to-skill@claude-code-skills`
- `workflow-builder@claude-code-skills`
- `caveman@claude-code-skills`
- `zero-hallucination-coder@claude-code-skills`
- `agent-harness@claude-code-skills`
- `memory-engineering@claude-code-skills`
- `skill-doctor@claude-code-skills`
- `grill-me@claude-code-skills`
- `handoff-engineering@claude-code-skills`
- `agile-product-owner@claude-code-skills`
- `capture-skill@claude-code-skills`
- `email-pair@claude-code-skills`
- `reflect-skill@claude-code-skills`
- `handoff-productivity@claude-code-skills`
- `andreessen@claude-code-skills`
- `roast@claude-code-skills`
- `fable-goal@claude-code-skills`
- `weekly-review@claude-code-skills`
- `deep-work@claude-code-skills`
- `meetings@claude-code-skills`
- `swedish-mentor@claude-code-skills`
- `landing@claude-code-skills`
- `linkedin@claude-code-skills`
- `pulse@claude-code-skills`
- `deep-research@claude-code-skills`
- `litreview@claude-code-skills`
- `grants@claude-code-skills`
- `dossier@claude-code-skills`
- `patent@claude-code-skills`
- `syllabus@claude-code-skills`
- `notebooklm@claude-code-skills`
- `research-orchestrator@claude-code-skills`
- `deepread@claude-code-skills`
- `aeo@claude-code-skills`
- `security-guidance@claude-code-skills`
- `skillopt-sleep@claude-code-skills`
- `business-operations-skills@claude-code-skills`
- `commercial-skills@claude-code-skills`
- `universal-scraping-architect@claude-code-skills`
- `research-ops-skills@claude-code-skills`
- `markdown-html-skills@claude-code-skills`
- `youtube-full@claude-code-skills`
- `compliance-os@claude-code-skills`
- `snowflake-development@claude-code-skills`
- `behuman@claude-code-skills`
- `claude-coach@claude-code-skills`
- `grill-with-docs@claude-code-skills`
- `llm-cost-optimizer@claude-code-skills`
- `prompt-governance@claude-code-skills`
- `business-investment-advisor@claude-code-skills`
- `video-content-strategist@claude-code-skills`
- `compliance-team-eu-ai-act@claude-code-skills`
- `compliance-team-iso42001@claude-code-skills`
- `collab-proof@claude-code-skills`
- `human-gate@claude-code-skills`
- `agent-launcher-skills@claude-code-skills`
- `agent-memory@claude-code-skills`
- `spinning-up-deep-rl@claude-code-skills`
- `deep-learning-book@claude-code-skills`

</details>

<details><summary><code>baoyu-skills</code> — JimLiu/baoyu-skills (1)</summary>

- `baoyu-skills@baoyu-skills`

</details>

<details><summary><code>spacetimedb-plugins</code> — clockworklabs/SpacetimeDB (1)</summary>

- `spacetimedb@spacetimedb-plugins`

</details>

<details><summary><code>promptfoo</code> — promptfoo/promptfoo (1)</summary>

- `promptfoo@promptfoo`

</details>

<details><summary><code>compound-engineering-plugin</code> — EveryInc/compound-engineering-plugin (1)</summary>

- `compound-engineering@compound-engineering-plugin`

</details>

<details><summary><code>voltagent-subagents</code> — VoltAgent/awesome-claude-code-subagents (10)</summary>

- `voltagent-core-dev@voltagent-subagents`
- `voltagent-lang@voltagent-subagents`
- `voltagent-infra@voltagent-subagents`
- `voltagent-qa-sec@voltagent-subagents`
- `voltagent-data-ai@voltagent-subagents`
- `voltagent-dev-exp@voltagent-subagents`
- `voltagent-domains@voltagent-subagents`
- `voltagent-biz@voltagent-subagents`
- `voltagent-meta@voltagent-subagents`
- `voltagent-research@voltagent-subagents`

</details>

<details><summary><code>knowledge-work-plugins</code> — anthropics/knowledge-work-plugins (113)</summary>

- `noibu@knowledge-work-plugins`
- `productivity@knowledge-work-plugins`
- `enterprise-search@knowledge-work-plugins`
- `cowork-plugin-management@knowledge-work-plugins`
- `sales@knowledge-work-plugins`
- `finance@knowledge-work-plugins`
- `data@knowledge-work-plugins`
- `legal@knowledge-work-plugins`
- `marketing@knowledge-work-plugins`
- `customer-support@knowledge-work-plugins`
- `product-management@knowledge-work-plugins`
- `bio-research@knowledge-work-plugins`
- `slack-by-salesforce@knowledge-work-plugins`
- `apollo@knowledge-work-plugins`
- `common-room@knowledge-work-plugins`
- `engineering@knowledge-work-plugins`
- `human-resources@knowledge-work-plugins`
- `design@knowledge-work-plugins`
- `operations@knowledge-work-plugins`
- `small-business@knowledge-work-plugins`
- `brand-voice@knowledge-work-plugins`
- `tavily@knowledge-work-plugins`
- `vanta-mcp-plugin@knowledge-work-plugins`
- `zoom-plugin@knowledge-work-plugins`
- `bigdata-com@knowledge-work-plugins`
- `miro@knowledge-work-plugins`
- `planetscale@knowledge-work-plugins`
- `adspirer-ads-agent@knowledge-work-plugins`
- `sanity-plugin@knowledge-work-plugins`
- `zoominfo@knowledge-work-plugins`
- `mintlify@knowledge-work-plugins`
- `daloopa@knowledge-work-plugins`
- `zapier@knowledge-work-plugins`
- `intercom@knowledge-work-plugins`
- `cockroachdb@knowledge-work-plugins`
- `prisma@knowledge-work-plugins`
- `fastly-agent-toolkit@knowledge-work-plugins`
- `cloudinary@knowledge-work-plugins`
- `nimble@knowledge-work-plugins`
- `brightdata-plugin@knowledge-work-plugins`
- `searchfit-seo@knowledge-work-plugins`
- `atlan@knowledge-work-plugins`
- `ai-firstify@knowledge-work-plugins`
- `product-tracking-skills@knowledge-work-plugins`
- `postiz@knowledge-work-plugins`
- `figma@knowledge-work-plugins`
- `adobe-for-creativity@knowledge-work-plugins`
- `pdf-viewer@knowledge-work-plugins`
- `box@knowledge-work-plugins`
- `lseg@knowledge-work-plugins`
- `sp-global@knowledge-work-plugins`
- `carta-cap-table@knowledge-work-plugins`
- `carta-crm@knowledge-work-plugins`
- `carta-investors@knowledge-work-plugins`
- `airtable@knowledge-work-plugins`
- `desktop-commander@knowledge-work-plugins`
- `qodo@knowledge-work-plugins`
- `qodo-standards@knowledge-work-plugins`
- `servicenow-sdk@knowledge-work-plugins`
- `twilio-developer-kit@knowledge-work-plugins`
- `vibe-prospecting@knowledge-work-plugins`
- `base44@knowledge-work-plugins`
- `wix@knowledge-work-plugins`
- `datadog@knowledge-work-plugins`
- `airwallex-agentos@knowledge-work-plugins`
- `langfuse@knowledge-work-plugins`
- `valtown@knowledge-work-plugins`
- `learn-with-coursera@knowledge-work-plugins`
- `monday-crm@knowledge-work-plugins`
- `monday-com@knowledge-work-plugins`
- `lusha@knowledge-work-plugins`
- `auth0@knowledge-work-plugins`
- `buildkite@knowledge-work-plugins`
- `clickhouse@knowledge-work-plugins`
- `datarobot-agent-skills@knowledge-work-plugins`
- `qdrant-skills@knowledge-work-plugins`
- `qt-development-skills@knowledge-work-plugins`
- `exa@knowledge-work-plugins`
- `dropbox@knowledge-work-plugins`
- `canva@knowledge-work-plugins`
- `pixeltable@knowledge-work-plugins`
- `grafana-assistant@knowledge-work-plugins`
- `grafana-cloud-mcp@knowledge-work-plugins`
- `grasp@knowledge-work-plugins`
- `honeycomb@knowledge-work-plugins`
- `b12-claude-plugin@knowledge-work-plugins`
- `signoz@knowledge-work-plugins`
- `tinyfish@knowledge-work-plugins`
- `carbone-skill@knowledge-work-plugins`
- `modern-web-guidance@knowledge-work-plugins`
- `stackhawk-api@knowledge-work-plugins`
- `stackhawk-hawkscan@knowledge-work-plugins`
- `growthbook@knowledge-work-plugins`
- `browser-use@knowledge-work-plugins`
- `gitkraken@knowledge-work-plugins`
- `synthflow@knowledge-work-plugins`
- `unity@knowledge-work-plugins`
- `unstructured-foundation@knowledge-work-plugins`
- `netsuite-ai-companion@knowledge-work-plugins`
- `netsuite-finance-analyst@knowledge-work-plugins`
- `blackrock-advisor-center-plugin@knowledge-work-plugins`
- `informatica-for-claude-platform@knowledge-work-plugins`
- `activecampaign@knowledge-work-plugins`
- `security-guidance@knowledge-work-plugins`
- `hubspot-sales@knowledge-work-plugins`
- `gc-ai@knowledge-work-plugins`
- `maven-bio@knowledge-work-plugins`
- `claude-for-financial-advisors@knowledge-work-plugins`
- `zocks-advisor@knowledge-work-plugins`
- `intuit-quickbooks@knowledge-work-plugins`
- `leadfeeder@knowledge-work-plugins`
- `chronograph-gp@knowledge-work-plugins`
- `chronograph-lp@knowledge-work-plugins`

</details>

<details><summary><code>pascal</code> — pascalorg/editor (1)</summary>

- `pascal-agent-skills@pascal`

</details>

<details><summary><code>hindsight</code> — vectorize-io/hindsight (2)</summary>

- `hindsight-memory@hindsight`
- `hindsight-zcode@hindsight`

</details>

<details><summary><code>open-code-review</code> — alibaba/open-code-review (1)</summary>

- `open-code-review@open-code-review`

</details>

<details><summary><code>context-mode</code> — mksglu/context-mode (1)</summary>

- `context-mode@context-mode`

</details>

<details><summary><code>watermarks-remover</code> — guillaumemeyer/watermarks-remover (1)</summary>

- `watermarks-remover@watermarks-remover`

</details>

<details><summary><code>ralph-marketplace</code> — snarktank/ralph (1)</summary>

- `ralph-skills@ralph-marketplace`

</details>

<details><summary><code>daily.dev</code> — dailydotdev/daily (2)</summary>

- `daily.dev@daily.dev`
- `daily-dev-ask@daily.dev`

</details>

<details><summary><code>google-plugins</code> — google/skills (17)</summary>

- `alloydb@google-plugins`
- `alloydb-omni@google-plugins`
- `bigtable@google-plugins`
- `cloud-sql-mysql@google-plugins`
- `cloud-sql-postgresql@google-plugins`
- `cloud-sql-sqlserver@google-plugins`
- `firestore-native@google-plugins`
- `data-agent-kit-starter-pack@google-plugins`
- `google-cloud-storage@google-plugins`
- `looker@google-plugins`
- `oracledb@google-plugins`
- `spanner@google-plugins`
- `knowledge-catalog@google-plugins`
- `dataproc@google-plugins`
- `bigquery@google-plugins`
- `db-context-engineering@google-plugins`
- `google-cloud-developer@google-plugins`

</details>

<details><summary><code>pua-skills</code> — tanweai/pua (1)</summary>

- `pua@pua-skills`

</details>

<details><summary><code>openseo</code> — every-app/open-seo (1)</summary>

- `openseo@openseo`

</details>

<details><summary><code>deepeval-plugins</code> — confident-ai/deepeval (1)</summary>

- `deepeval@deepeval-plugins`

</details>

<details><summary><code>context-engineering-marketplace</code> — muratcankoylan/Agent-Skills-for-Context-Engineering (1)</summary>

- `context-engineering@context-engineering-marketplace`

</details>

<details><summary><code>browser-harness</code> — browser-use/browser-harness (1)</summary>

- `browser-harness@browser-harness`

</details>

<details><summary><code>claude-video</code> — bradautomates/claude-video (1)</summary>

- `watch@claude-video`

</details>

<details><summary><code>agricidaniel-claude-seo</code> — AgriciDaniel/claude-seo (1)</summary>

- `claude-seo@agricidaniel-claude-seo`

</details>

<details><summary><code>ag-ui</code> — ag-ui-protocol/ag-ui (1)</summary>

- `ag-ui-dotnet@ag-ui`

</details>

<details><summary><code>ego-agent-skills</code> — citrolabs/ego-lite (1)</summary>

- `browser-skills@ego-agent-skills`

</details>

<details><summary><code>pipecat-dev-skills</code> — pipecat-ai/pipecat (1)</summary>

- `pipecat-dev@pipecat-dev-skills`

</details>

<details><summary><code>text-to-cad</code> — earthtojake/text-to-cad (1)</summary>

- `cad@text-to-cad`

</details>

<details><summary><code>gsap-skills</code> — greensock/gsap-skills (1)</summary>

- `gsap-skills@gsap-skills`

</details>

<details><summary><code>agricidaniel-claude-obsidian</code> — AgriciDaniel/claude-obsidian (1)</summary>

- `claude-obsidian@agricidaniel-claude-obsidian`

</details>

<details><summary><code>superpowers-marketplace</code> — obra/superpowers-marketplace (10)</summary>

- `superpowers@superpowers-marketplace`
- `superpowers-chrome@superpowers-marketplace`
- `elements-of-style@superpowers-marketplace`
- `episodic-memory@superpowers-marketplace`
- `superpowers-lab@superpowers-marketplace`
- `superpowers-developing-for-claude-code@superpowers-marketplace`
- `superpowers-dev@superpowers-marketplace`
- `claude-session-driver@superpowers-marketplace`
- `private-journal-mcp@superpowers-marketplace`
- `double-shot-latte@superpowers-marketplace`

</details>

## Skills vendorizadas

`.claude/skills/caveman/` — só a skill de compressão, copiada do repo upstream
(MIT). As outras 19 do pack ficaram de fora porque juntas custavam cerca de 1.100
tokens de índice por sessão sem uso proporcional; o critério, skill a skill, está
em `.claude/skills/CAVEMAN.md`. Independe de plugin: funciona inclusive onde
`/plugin` não existe, como o Claude Code na web.
