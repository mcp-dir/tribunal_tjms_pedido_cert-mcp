---
name: tribunal_tjms_pedido_cert-mcp
description: Skill da REST API do Tribunal TJMS: Cadastro de Pedido de Certidão (1º grau) na MCP.AI: 1 endpoint em /api/tribunal_tjms_pedido_cert. Tribunal TJMS: Cadastro de Pedido de Certidão (1º grau), consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago. Autentique com workspace API key (sk_live) gerada em app.mcp.ai/settings/api-keys. Use quando o usuário pedir algo coberto pelos endpoints.
---

# Tribunal TJMS: Cadastro de Pedido de Certidão (1º grau) — REST API skill

Você tem acesso à **Tribunal TJMS: Cadastro de Pedido de Certidão (1º grau)** REST API na MCP.AI.

> Tribunal TJMS: Cadastro de Pedido de Certidão (1º grau), consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago.

## Base URL

```
https://api.mcp.ai/api/tribunal_tjms_pedido_cert
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
curl -X POST https://api.mcp.ai/api/tribunal_tjms_pedido_cert/consultar \
  -H "Authorization: Bearer sk_live_..." \
  -H "Content-Type: application/json" \
  -d '{"comarca":"...","modelo":"...","nome_razao_social":"...","email":"..."}'
```

## Reportar problemas

Se um endpoint retornar erro, vazio ou dado inesperado, reporte (não desista calado): **POST /api/tribunal_tjms_pedido_cert/report** com `{ "message": "...", "context"?: "...", "conversation"?: [...] }`. Isso notifica o time da MCP.AI.

## Endpoints (1)

#### `tribunal_tjms_pedido_cert_consultar`

Tribunal TJMS: Cadastro de Pedido de Certidão (1º grau), consulta em fonte oficial. _(POST /api/tribunal_tjms_pedido_cert/consultar)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `comarca` | string | Sim | Parâmetro de consulta "comarca". |
| `modelo` | string | Sim | Parâmetro de consulta "modelo". |
| `nome_razao_social` | string | Sim | Parâmetro de consulta "nome_razao_social". |
| `cpf` | string | Não | Parâmetro de consulta "cpf". |
| `cnpj` | string | Não | Parâmetro de consulta "cnpj". |
| `rg` | string | Não | Parâmetro de consulta "rg". |
| `genero` | string | Não | Parâmetro de consulta "genero". |
| `nome_pai` | string | Não | Parâmetro de consulta "nome_pai". |
| `nome_mae` | string | Não | Parâmetro de consulta "nome_mae". |
| `birthdate` | string | Não | Parâmetro de consulta "birthdate". |
| `email` | string | Sim | Parâmetro de consulta "email". |

---

Este MCP também funciona via **conexão MCP** (Claude / Cursor) em `https://api.mcp.ai/p_tribunal_tjms_pedido_cert` — veja o [README](../../README.md). A skill acima é pra consumir a **REST API** direto (agente próprio / código).
