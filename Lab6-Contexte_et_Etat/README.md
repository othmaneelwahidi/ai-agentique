# Lab 6 — Contexte et état

Exemples qui distinguent les informations fournies pour une invocation du graphe et les données conservées dans son état.

**Auteur : Othmane El Wahidi El Alaoui**

## Fichiers

- `agent_context.py` : transmet un profil de lecteur comme contexte d’exécution ;
- `agent_state.py` : conserve les informations de bibliothèque dans un état personnalisé ;
- `pyproject.toml` : dépendances ;
- PDF/ODT : énoncé du TP.

## Installation et exécution

```bash
uv sync
ollama pull llama3.2:3b
uv run python agent_context.py
uv run python agent_state.py
```

Le contexte configure une exécution sans faire partie de l’historique métier. L’état, lui, circule entre les nœuds et peut être sauvegardé par un checkpointer.
