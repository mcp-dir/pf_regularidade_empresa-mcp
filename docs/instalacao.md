# Instalação detalhada

Polícia Federal: Situação e Regularidade de Empresa de Segurança Privada é um servidor MCP remoto. Aponte seu cliente pra `https://api.mcp.ai/p_pf_regularidade_empresa`. Snippets rápidos: [INSTALL.md](../INSTALL.md).

| Cliente | URL | Auth |
|---|---|---|
| Claude Desktop | `https://api.mcp.ai/p_pf_regularidade_empresa` | OAuth 2.1 ou agent-auth |
| Cursor | `https://api.mcp.ai/p_pf_regularidade_empresa` | OAuth 2.1 ou agent-auth |
| VS Code (Copilot) | `https://api.mcp.ai/p_pf_regularidade_empresa` | OAuth 2.1 ou agent-auth |

A config JSON é a mesma em todos: só a URL, sem headers.

## Desinstalar

Remova o bloco `mcpServers.pf_regularidade_empresa` (ou `servers.pf_regularidade_empresa` no VS Code) do config do cliente e reinicie.
