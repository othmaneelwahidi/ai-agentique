# Lab 3 — RAG et agent SQL

Deux approches d’accès à des connaissances externes : recherche sémantique dans un document PDF et génération de requêtes sur une base SQLite.

**Auteur : Othmane El Wahidi El Alaoui**

## Contenu

| Fichier | Rôle |
|---|---|
| `part1_rag_pdf.py` | Charge le manuel employé, découpe son texte, crée les embeddings et répond à partir des passages retrouvés |
| `acmecorp-employee-handbook.pdf` | Document utilisé par le pipeline RAG |
| `part2_sql_agent.py` | Crée un agent capable d’interroger SQLite avec des outils SQL |
| `Chinook.db` | Base musicale de démonstration |
| `3 TP Agent RAG.pdf` | Énoncé du TP |

## Installation

Ce dossier ne contient pas de manifeste de dépendances. Créez un environnement virtuel puis installez les imports requis par les deux scripts, notamment LangChain, LangGraph, Ollama, les connecteurs communautaires, `pypdf` et les embeddings Hugging Face.

Ollama et `llama3.2:3b` doivent être disponibles :

```bash
ollama pull llama3.2:3b
python part1_rag_pdf.py
python part2_sql_agent.py
```

Les chemins vers le PDF et la base sont relatifs au dossier : lancez les commandes depuis `Lab3-RAG`.
