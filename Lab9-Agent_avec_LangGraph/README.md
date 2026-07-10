# Lab 9 — Agent avec LangGraph

Construction manuelle d’un agent outillé, puis ajout d’une validation humaine, de checkpoints, d’un historique et d’un fork d’exécution.

**Auteur : Othmane El Wahidi El Alaoui**

## Fichiers

| Fichier | Rôle |
|---|---|
| `tools_setup.py` | Modèle local et outils arithmétiques |
| `agent_node.py` | Agent représenté comme nœud d’un `StateGraph` |
| `hitl_workflow.py` | Workflow fonctionnel avec `@entrypoint`, `@task` et interruption |
| `tp_advanced_agent.py` | Démonstration avancée : approbation, rejet, historique et fork |

## Installation et exécution

```bash
uv sync
ollama pull llama3.2:3b
uv run python agent_node.py
uv run python hitl_workflow.py
uv run python tp_advanced_agent.py
```

Chaque scénario utilise un `thread_id`. Conservez-le lors d’une reprise et utilisez un identifiant différent pour isoler deux conversations.
