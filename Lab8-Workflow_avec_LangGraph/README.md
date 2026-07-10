# Lab 8 — Workflows avec LangGraph

Collection de petits graphes qui présentent progressivement l’état, les reducers, les routes conditionnelles et les boucles.

**Auteur : Othmane El Wahidi El Alaoui**

## Exemples

| Fichier | Concept |
|---|---|
| `hello_graph.py` | Graphe minimal et enchaînement de nœuds |
| `workflows/two_step_workflow.py` | Pipeline en deux étapes |
| `reducers_demo.py` | Fusion des mises à jour d’état avec un reducer |
| `message_state.py` | État spécialisé pour les messages |
| `conditional_workflow.py` | Branchement selon une condition |
| `workflow_loop.py` | Boucle contrôlée et condition de sortie |

## Installation et exécution

```bash
uv sync
uv run python hello_graph.py
uv run python workflows/two_step_workflow.py
uv run python reducers_demo.py
uv run python message_state.py
uv run python conditional_workflow.py
uv run python workflow_loop.py
```

Certains exemples peuvent utiliser Ollama ; dans ce cas, démarrez-le et installez `llama3.2:3b`.
