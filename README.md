# AI Agentique — Master BDCC

Travaux pratiques consacrés à l’ingénierie des prompts, LangChain, RAG, MCP et LangGraph.

**Auteur : Othmane El Wahidi El Alaoui**

## Parcours du dépôt

| Dossier | Contenu |
|---|---|
| [`Lab1-prompt-engineering`](./Lab1-prompt-engineering/) | Tokenisation, modèles locaux/distants, sorties structurées et traitement d’images |
| [`Lab2-langchain-agents`](./Lab2-langchain-agents/) | Agent LangChain de chef personnel avec outils et mémoire |
| [`Lab3-RAG`](./Lab3-RAG/) | Recherche dans un PDF et interrogation de la base SQLite Chinook |
| [`Lab4-MCP`](./Lab4-MCP/) | Serveurs et clients MCP via stdio, serveur distant et HTTP |
| [`Lab5-LangGraph_Studio`](./Lab5-LangGraph_Studio/) | Visualisation LangGraph Studio et orchestration multi-agents |
| [`Lab6-Contexte_et_Etat`](./Lab6-Contexte_et_Etat/) | Différence entre contexte d’exécution et état persistant |
| [`Lab7-Human_In_The_Loop`](./Lab7-Human_In_The_Loop/) | Approbation, refus ou modification d’actions sensibles |
| [`Lab8-Workflow_avec_LangGraph`](./Lab8-Workflow_avec_LangGraph/) | Graphes, reducers, branchements et boucles |
| [`Lab9-Agent_avec_LangGraph`](./Lab9-Agent_avec_LangGraph/) | Outils, nœuds agent, checkpoints, historique et fork |
| [`TP-Chef_personnel`](./TP-Chef_personnel/) | Assistant culinaire avec RAG, mémoire et recherche web optionnelle |
| [`Evaluation-finale`](./Evaluation-finale/) | Prototype d’assistant RAG d’éducation financière |

Chaque dossier possède son propre README avec les prérequis, les fichiers utiles et les commandes d’exécution.

## Prérequis généraux

- Python 3.10 ou version ultérieure ;
- [`uv`](https://docs.astral.sh/uv/) pour les projets qui contiennent `pyproject.toml` ;
- [Ollama](https://ollama.com/) et le modèle local `llama3.2:3b` pour la majorité des exemples ;
- des clés API uniquement pour les scripts qui utilisent Groq, OpenAI, Tavily ou LangSmith.

```bash
ollama pull llama3.2:3b
```

## Démarrage rapide

Ouvrez le dossier du lab souhaité, lisez son README, puis installez ses dépendances. Exemple :

```bash
cd Lab8-Workflow_avec_LangGraph
uv sync
uv run python hello_graph.py
```

Ne versionnez jamais les fichiers `.env` ni les clés API.
