# Lab 4 — Model Context Protocol (MCP)

Démonstrations de connexion d’un agent LangChain à des outils exposés avec MCP selon plusieurs transports.

**Auteur : Othmane El Wahidi El Alaoui**

## Fichiers

| Fichier | Rôle |
|---|---|
| `mcp_local_server.py` | Serveur MCP local lancé comme sous-processus stdio |
| `agentMCP.py` | Client/agent connecté au serveur local |
| `agentMCPTime.py` | Agent connecté à un serveur MCP de temps |
| `mcp_http_server.py` | Serveur MCP accessible en HTTP |
| `agentMCPDistant.py` | Client du serveur MCP distant |

Les fichiers PDF et ODT contiennent l’énoncé du TP.

## Installation

```bash
uv sync
ollama pull llama3.2:3b
```

Selon l’exemple, ajoutez les éventuelles clés API dans un fichier `.env` local.

## Exécution

Serveur local via stdio :

```bash
uv run python agentMCP.py
```

Serveur HTTP et client, dans deux terminaux :

```bash
uv run python mcp_http_server.py
uv run python agentMCPDistant.py
```

Pour l’exemple de temps : `uv run python agentMCPTime.py`. Vérifiez l’adresse et le port configurés dans les scripts avant de lancer les exemples réseau.
