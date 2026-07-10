# Lab 7 — Human in the Loop

Agent LangGraph qui suspend une action sensible afin qu’un humain puisse l’approuver, la refuser ou la modifier avant exécution.

**Auteur : Othmane El Wahidi El Alaoui**

## Contenu

- `agent_hitl.py` : agent, outil sensible, interruption et scénarios de reprise ;
- `pyproject.toml` : dépendances ;
- PDF/ODT : énoncé du TP.

## Installation et exécution

```bash
uv sync
ollama pull llama3.2:3b
uv run python agent_hitl.py
```

Le checkpointer associe la suspension à un `thread_id`. La reprise doit donc réutiliser la même configuration. Les actions de démonstration sont simulées : vérifiez toujours l’outil avant de le relier à un service réel.
