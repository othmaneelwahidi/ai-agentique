# TP — Chef personnel

Assistant culinaire qui recherche des recettes locales, mémorise les préférences alimentaires et peut compléter ses résultats avec Tavily.

**Auteur : Othmane El Wahidi El Alaoui**

## Architecture

`chef_agent.py` indexe `recipes.txt` dans un `InMemoryVectorStore` avec les embeddings `all-MiniLM-L6-v2`. L’agent Ollama dispose de quatre outils :

| Outil | Fonction |
|---|---|
| `search_recipes_rag` | Recherche sémantique dans les recettes locales |
| `search_web` | Recherche Tavily optionnelle |
| `remember_preference` | Ajoute une préférence, allergie ou restriction à l’état |
| `get_preferences` | Relit les préférences de la session |

La mémoire repose sur `InMemorySaver` et reste liée au `thread_id`; elle n’est pas persistée après l’arrêt du programme.

## Installation

```bash
uv sync
ollama pull llama3.2:3b
```

Pour activer la recherche web, créez un fichier `.env` non versionné contenant `TAVILY_API_KEY`. Sans clé, l’agent continue avec la base locale.

## Exécution

```bash
uv run python chef_agent.py
```

Le script lance une démonstration prédéfinie. `exercice.md` contient l’énoncé original et `recipes.txt` la base de quinze recettes.
