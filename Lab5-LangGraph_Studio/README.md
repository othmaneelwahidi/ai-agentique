# Lab 5 — LangGraph Studio et multi-agents

Ce lab montre comment exposer des graphes dans LangGraph Studio, les inspecter et coordonner plusieurs agents spécialisés.

**Auteur : Othmane El Wahidi El Alaoui**

## Contenu

- `agent_simple.py` : agent minimal utilisable dans Studio ;
- `multi_agents.py` : orchestration hiérarchique de plusieurs agents ;
- `langgraph.json` : points d’entrée chargés par LangGraph CLI ;
- `pyproject.toml` : dépendances du lab ;
- documents PDF/ODT : supports LangGraph Studio et multi-agents.

## Installation

```bash
uv sync
ollama pull llama3.2:3b
```

Si le suivi LangSmith est utilisé, placez `LANGSMITH_API_KEY` dans un fichier `.env` local.

## Utilisation

Lancer l’interface de développement :

```bash
uv run langgraph dev
```

Lancer directement la démonstration multi-agents :

```bash
uv run python multi_agents.py
```

`langgraph.json` déclare les graphes disponibles ; mettez-le à jour si un module ou une variable de graphe est renommé.
