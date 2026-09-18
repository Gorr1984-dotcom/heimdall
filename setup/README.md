# Setup global do Claude Code

Configuração enxuta para `~/.claude/`, feita para não gastar contexto à toa.
Nada aqui é aplicado automaticamente: são arquivos para copiar para a sua máquina.

## Instalar

```bash
mkdir -p ~/.claude

# guarde o que já existe antes de qualquer cópia
cp ~/.claude/CLAUDE.md     ~/.claude/CLAUDE.md.bak     2>/dev/null
cp ~/.claude/settings.json ~/.claude/settings.json.bak 2>/dev/null

cp setup/claude-global/CLAUDE.md ~/.claude/CLAUDE.md
cp setup/claude-global/settings.json ~/.claude/settings.json
```

Se você já tinha um `settings.json`, o comando acima o substitui — abra o `.bak` e
traga de volta o que era seu (`permissions`, `env`, `hooks`, `model`). O arquivo
daqui só define `permissions.allow`, `extraKnownMarketplaces` e `enabledPlugins`.

Quer o modo caveman em todo projeto, e não só neste repo:

```bash
mkdir -p ~/.claude/skills/caveman
cp -r .claude/skills/caveman/. ~/.claude/skills/caveman/
```

## O que cada arquivo faz

### `CLAUDE.md` (~150 tokens)

Preferência de saída e de trabalho, aplicada automaticamente em toda sessão.
Faz o trabalho do dia a dia que a skill `caveman` faria, sem precisar invocar nada.
Mantenha curto: este arquivo entra no contexto de **toda** sessão, então cada linha
que você acrescenta é cobrada para sempre. Regra prática: se você não conseguir
justificar a linha, ela sai.

### `settings.json`

- `permissions.allow`: comandos de leitura pré-aprovados. Menos prompt de permissão
  significa menos ida e volta, e ida e volta custa contexto.
- `extraKnownMarketplaces`: 4 marketplaces registrados. Registrar é só descoberta —
  token zero, apenas um clone raso por repositório.
- `enabledPlugins`: vazio de propósito. Habilitar plugin é o que custa: cada skill
  dele entra no índice de toda sessão, e hooks executam comandos na sua máquina.

## Auditoria — onde está o gasto de verdade

Ajustar arquivo de config rende pouco perto disto. Por ordem de impacto:

1. **Plugins habilitados na conta.** Cada skill de cada plugin injeta nome e
   descrição no índice de **toda** sessão, tenha ou não a ver com o que você está
   fazendo. Skill de domínio muito específico — LMS, painel de BI, registry de
   projetos — pesa igual numa sessão de Go. Habilite por projeto, não globalmente.
   Ver com `/plugin`.
2. **Servidores MCP ativos.** Costumam ser o item mais caro: o schema de todas as
   ferramentas de cada servidor entra no contexto. Ver com `claude mcp list` e
   desligar o que não usa no dia a dia.
3. **`CLAUDE.md` inchado**, global ou de projeto. O erro comum é ele virar
   documentação. Documentação vai para `docs/`; `CLAUDE.md` é só o que muda o
   comportamento do agente.
4. **Skills vendorizadas** em `.claude/skills/`. Mesma lógica dos plugins.

Meça antes e depois com `/context`, que mostra a divisão do uso de contexto da
sessão. É o número que importa — o resto é estimativa.

## Referência

`.claude/PLUGINS.md` cataloga 95 marketplaces e 886 plugins, com o identificador
pronto de cada um. É documentação: não entra em contexto, não custa nada, e serve
para achar algo quando precisar em vez de deixar tudo habilitado por via das dúvidas.
