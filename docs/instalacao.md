# Instalação detalhada

Tribunal TJMS: Cadastro de Pedido de Certidão (1º grau) é um servidor MCP remoto. Aponte seu cliente pra `https://api.mcp.ai/p_tribunal_tjms_pedido_cert`. Snippets rápidos: [INSTALL.md](../INSTALL.md).

| Cliente | URL | Auth |
|---|---|---|
| Claude Desktop | `https://api.mcp.ai/p_tribunal_tjms_pedido_cert` | OAuth 2.1 ou agent-auth |
| Cursor | `https://api.mcp.ai/p_tribunal_tjms_pedido_cert` | OAuth 2.1 ou agent-auth |
| VS Code (Copilot) | `https://api.mcp.ai/p_tribunal_tjms_pedido_cert` | OAuth 2.1 ou agent-auth |

A config JSON é a mesma em todos: só a URL, sem headers.

## Desinstalar

Remova o bloco `mcpServers.tribunal_tjms_pedido_cert` (ou `servers.tribunal_tjms_pedido_cert` no VS Code) do config do cliente e reinicie.
