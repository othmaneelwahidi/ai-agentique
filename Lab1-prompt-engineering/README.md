# Lab 1 — Ingénierie des prompts

Exemples progressifs pour comprendre la tokenisation, appeler plusieurs fournisseurs de modèles et obtenir des réponses structurées ou multimodales.

**Auteur : Othmane El Wahidi El Alaoui**

## Fichiers

| Fichier | Rôle |
|---|---|
| `01_tokenisation.py` | Compte et inspecte les tokens avec `tiktoken` |
| `02_ollama_prompt.py` | Envoie un prompt à un modèle Ollama local |
| `03_groq_prompt.py` | Utilise un modèle hébergé par Groq |
| `04_openai_prompt.py` | Utilise l’API OpenAI |
| `05_aspect_sentiment_json.py` | Produit une analyse de sentiment structurée en JSON |
| `06_image_generation.py` | Génère une image à partir d’un prompt |
| `07_image_description.py` | Décrit une image avec un modèle multimodal |
| `rag.png` | Image d’exemple utilisée par les exercices |

## Installation et configuration

```bash
uv sync
```

Créez un fichier `.env` local selon les scripts exécutés : `GROQ_API_KEY` pour Groq et `OPENAI_API_KEY` pour OpenAI. Ollama doit être lancé pour l’exemple local.

## Exécution

```bash
uv run python 01_tokenisation.py
uv run python 02_ollama_prompt.py
```

Remplacez le nom du script pour lancer un autre exemple. Les appels aux services distants peuvent être facturés par leur fournisseur.
