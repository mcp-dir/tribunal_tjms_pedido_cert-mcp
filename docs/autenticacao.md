# Autenticação

Tribunal TJMS: Cadastro de Pedido de Certidão (1º grau) usa um único endpoint público (`https://api.mcp.ai/p_tribunal_tjms_pedido_cert`).

Dois fluxos, escolhidos automaticamente pelo cliente:

- **OAuth 2.1** (recomendado, cliente moderno) — browser abre na 1ª chamada, login via magic-link, token rotaciona sozinho, nunca passa pelo chat.
- **agent-auth** (cliente sem OAuth) — o agente expõe a tool `authenticate(token)`. Você abre `https://app.mcp.ai/agent-auth`, faz login, copia o JWT e cola no chat. ⚠️ o JWT passa pelo provedor LLM — rotacione periodicamente.

Config do cliente nos dois casos:
```json
{ "mcpServers": { "tribunal_tjms_pedido_cert": { "url": "https://api.mcp.ai/p_tribunal_tjms_pedido_cert" } } }
```
