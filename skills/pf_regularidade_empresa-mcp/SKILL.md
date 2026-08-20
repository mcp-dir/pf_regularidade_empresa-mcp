---
name: pf_regularidade_empresa-mcp
description: Skill da REST API do Polícia Federal: Situação e Regularidade de Empresa de Segurança Privada na MCP.AI: 1 endpoint em /api/pf_regularidade_empresa. Polícia Federal: Situação e Regularidade de Empresa de Segurança Privada, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago. Autentique com workspace API key (sk_live) gerada em app.mcp.ai/settings/api-keys. Use quando o usuário pedir algo coberto pelos endpoints.
---

# Polícia Federal: Situação e Regularidade de Empresa de Segurança Privada — REST API skill

Você tem acesso à **Polícia Federal: Situação e Regularidade de Empresa de Segurança Privada** REST API na MCP.AI.

> Polícia Federal: Situação e Regularidade de Empresa de Segurança Privada, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago.

## Base URL

```
https://api.mcp.ai/api/pf_regularidade_empresa
```

Todo endpoint é um **POST** na Base URL + o path abaixo. Os parâmetros vão no corpo JSON.

## Autenticação

Inclua em toda request:

```
Authorization: Bearer sk_live_...
Content-Type: application/json
```

> Gere sua chave em **https://app.mcp.ai/settings/api-keys** (workspace API key `sk_live_…`, não expira, revogável). Uma única chave serve pra todos os seus MCPs.

## Formato de resposta

```json
{ "ok": true, "tool": "<tool_id>", "result": <payload> }
```

## Exemplo cURL

```bash
curl -X POST https://api.mcp.ai/api/pf_regularidade_empresa/consultar \
  -H "Authorization: Bearer sk_live_..." \
  -H "Content-Type: application/json" \
  -d '{"cnpj":"..."}'
```

## Reportar problemas

Se um endpoint retornar erro, vazio ou dado inesperado, reporte (não desista calado): **POST /api/pf_regularidade_empresa/report** com `{ "message": "...", "context"?: "...", "conversation"?: [...] }`. Isso notifica o time da MCP.AI.

## Endpoints (1)

#### `pf_regularidade_empresa_consultar`

Polícia Federal: Situação e Regularidade de Empresa de Segurança Privada, consulta em fonte oficial. _(POST /api/pf_regularidade_empresa/consultar)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `login_cpf` | string | Não | Parâmetro de consulta "login_cpf". |
| `login_senha` | string | Não | Parâmetro de consulta "login_senha". |
| `pkcs12_cert` | string | Não | Parâmetro de consulta "pkcs12_cert". |
| `pkcs12_pass` | string | Não | Parâmetro de consulta "pkcs12_pass". |
| `cnpj` | string | Sim | Parâmetro de consulta "cnpj". |

---

Este MCP também funciona via **conexão MCP** (Claude / Cursor) em `https://api.mcp.ai/p_pf_regularidade_empresa` — veja o [README](../../README.md). A skill acima é pra consumir a **REST API** direto (agente próprio / código).
