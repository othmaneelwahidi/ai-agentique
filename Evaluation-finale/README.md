# Évaluation finale — Agentic RAG financier

Prototype LangGraph d’un assistant francophone d’éducation financière : budget, épargne, crédit, investissement et surendettement.

**Auteur : Othmane El Wahidi El Alaoui**

## Fonctionnement prévu

Le graphe défini dans `src/graph.py` fait alterner un agent Ollama et ses outils. Après une recherche documentaire, il évalue la pertinence des passages et peut reformuler la question jusqu’à deux fois. `InMemorySaver` conserve la conversation par `thread_id` pendant l’exécution.

Les composants configurés sont :

- Ollama `llama3.2:3b` pour le raisonnement ;
- embeddings `sentence-transformers/all-MiniLM-L6-v2` ;
- Chroma pour l’index vectoriel ;
- LangGraph pour l’orchestration.

## État actuel du dossier

Le dépôt ne contient pas encore `src/tools.py` ni `src/vectorstore.py`, pourtant importés par `src/graph.py` et `ingest.py`. Les PDF de données et leurs scripts de téléchargement sont également absents. En conséquence, `main.py`, `ingest.py`, `generate_graph.py` et l’évaluation ne sont pas exécutables dans l’état actuel. `graph.mmd` et `graph.png` montrent l’architecture générée précédemment.

## Fichiers présents

- `main.py` : interface de conversation en ligne de commande ;
- `ingest.py` : point d’entrée prévu pour construire l’index Chroma ;
- `generate_graph.py` : export Mermaid/PNG du graphe ;
- `src/config.py`, `src/llm.py`, `src/state.py`, `src/graph.py` : configuration et logique du graphe ;
- `evaluation/` : vingt questions et script de mesure ;
- PDF : sujet de l’évaluation finale.

## Installation prévue

```bash
uv sync --group dev
ollama pull llama3.2:3b
```

Une fois les modules et documents manquants ajoutés :

```bash
uv run python ingest.py
uv run python main.py
uv run python -m evaluation.run_evaluation
```

Les calculs fournis par cet assistant sont pédagogiques et ne constituent pas un conseil financier.
