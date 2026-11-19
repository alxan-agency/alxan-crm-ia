# Alxan CRM com a sua IA

Conecte o Claude Code, o Codex, o Cursor ou o claude.ai à sua conta do Alxan CRM e peça em português o
que hoje você faz clicando: conversas abertas sem responsável, leads parados no funil, resumo do dia,
etiquetas, respostas rápidas, agenda, cadências de follow-up.

A skill é curta de propósito. O conhecimento vem do próprio CRM, que se atualiza a cada versão: as
ferramentas do MCP (só as dos módulos do seu plano) e a Central de Ajuda
(https://crm.alxan.com.br/hc/ajuda). Os mapas em `skills/alxan-crm/references/` são refeitos a cada
atualização do Alxan CRM.

## Antes de começar

No Alxan CRM, como administrador: **Configurações → MCP → Novo perfil**. Comece com **somente
leitura**. A tela mostra um **endereço** e um **segredo** (o segredo aparece uma única vez).

## Claude Code (recomendado)

```bash
claude plugin marketplace add alxan-agency/alxan-crm-ia
claude plugin install alxan-crm@alxan-crm
```

O Claude Code pede o endereço e o segredo do perfil numa janela própria e guarda no cofre do sistema.
Digite o segredo só ali, nunca na conversa. Para trocar depois: `/plugin configure alxan-crm@alxan-crm`.

Atualizar: `claude plugin marketplace update alxan-crm` e `claude plugin update alxan-crm@alxan-crm`.

## Codex

```bash
codex plugin marketplace add alxan-agency/alxan-crm-ia
codex plugin add alxan-crm@alxan-crm
```

E o conector em `~/.codex/config.toml`, com o segredo na variável `ALXAN_CRM_MCP_TOKEN`:

```toml
[mcp_servers.alxan-crm]
url = "<ENDEREÇO>"
bearer_token_env_var = "ALXAN_CRM_MCP_TOKEN"
```

## Cursor e outros agentes

```bash
git clone --depth 1 https://github.com/alxan-agency/alxan-crm-ia.git
cp -R alxan-crm-ia/skills/alxan-crm .cursor/skills/      # ou ~/.agents/skills/, ~/.claude/skills/
```

Conector em `~/.cursor/mcp.json`:

```json
{ "mcpServers": { "alxan-crm": { "url": "<ENDEREÇO>",
  "headers": { "Authorization": "Bearer <SEGREDO>" } } } }
```

## claude.ai (navegador e aplicativo)

1. Personalizar → Conectores → Adicionar → **Adicionar conector personalizado**.
2. Endereço: o do perfil, trocando `/mcp/c/` por `/mcp/oauth/c/`. O claude.ai detecta o login sozinho:
   você entra no Alxan CRM e autoriza. Nenhum segredo é digitado.
3. Skill: compacte a pasta `skills/alxan-crm` em .zip e envie em Personalizar → Skills.

## Teste

Peça: *"Use a skill alxan-crm. Quantas conversas abertas eu tenho, por caixa de entrada?"*

## Segurança

- A IA só alcança os módulos do seu plano e só faz o que o usuário do perfil pode fazer na tela.
- Tudo que sai para o seu cliente pede a sua confirmação. Campanha, cadência e robô nascem em rascunho.
- Para cortar o acesso: Configurações → MCP → **Rotacionar token** ou **Excluir**. Vale na hora.

Suporte: time da Alxan.
