---
name: tribunal_trf3_certidao_distr-mcp
description: Skill da REST API do Tribunal TRF3: Certidão de Distribuição na MCP.AI: 1 endpoint em /api/tribunal_trf3_certidao_distr. Tribunal TRF3: Certidão de Distribuição, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago. Autentique com workspace API key (sk_live) gerada em app.mcp.ai/settings/api-keys. Use quando o usuário pedir algo coberto pelos endpoints.
---

# Tribunal TRF3: Certidão de Distribuição — REST API skill

Você tem acesso à **Tribunal TRF3: Certidão de Distribuição** REST API na MCP.AI.

> Tribunal TRF3: Certidão de Distribuição, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago.

## Base URL

```
https://api.mcp.ai/api/tribunal_trf3_certidao_distr
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
curl -X POST https://api.mcp.ai/api/tribunal_trf3_certidao_distr/consultar \
  -H "Authorization: Bearer sk_live_..." \
  -H "Content-Type: application/json" \
  -d '{}'
```

## Reportar problemas

Se um endpoint retornar erro, vazio ou dado inesperado, reporte (não desista calado): **POST /api/tribunal_trf3_certidao_distr/report** com `{ "message": "...", "context"?: "...", "conversation"?: [...] }`. Isso notifica o time da MCP.AI.

## Endpoints (1)

#### `tribunal_trf3_certidao_distr_consultar`

Tribunal TRF3: Certidão de Distribuição, consulta em fonte oficial. _(POST /api/tribunal_trf3_certidao_distr/consultar)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `abrangencia` | string | Não | Parâmetro de consulta "abrangencia". |
| `tipo` | string | Não | Parâmetro de consulta "tipo". |
| `cpf` | string | Não | Parâmetro de consulta "cpf". |
| `cnpj` | string | Não | Parâmetro de consulta "cnpj". |
| `nome` | string | Não | Parâmetro de consulta "nome". |
| `razao_social` | string | Não | Parâmetro de consulta "razao_social". |
| `nome_social` | string | Não | Parâmetro de consulta "nome_social". |
| `nome_mae` | string | Não | Parâmetro de consulta "nome_mae". |
| `birthdate` | string | Não | Parâmetro de consulta "birthdate". |
| `tipo_documento` | string | Não | Parâmetro de consulta "tipo_documento". |
| `documento` | string | Não | Parâmetro de consulta "documento". |
| `endereco` | string | Não | Parâmetro de consulta "endereco". |
| `tipo_telefone` | string | Não | Parâmetro de consulta "tipo_telefone". |
| `telefone` | string | Não | Parâmetro de consulta "telefone". |

---

Este MCP também funciona via **conexão MCP** (Claude / Cursor) em `https://api.mcp.ai/p_tribunal_trf3_certidao_distr` — veja o [README](../../README.md). A skill acima é pra consumir a **REST API** direto (agente próprio / código).
