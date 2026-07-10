# Lab 2 — Agents avec LangChain

Ce lab construit un assistant de cuisine capable d’utiliser des outils, de prendre en compte les ingrédients disponibles et de conserver le contexte d’une conversation.

**Auteur : Othmane El Wahidi El Alaoui**

## Contenu

- `chef_personnel_agent.py` : implémentation et démonstration de l’agent ;
- `requirements.txt` : dépendances Python ;
- `images/` : captures d’écran des exécutions ;
- documents DOCX/ODT : énoncé du TP.

## Installation

```bash
python -m venv .venv
# Windows PowerShell
.venv\Scripts\Activate.ps1
pip install -r requirements.txt
```

L’exemple utilise Ollama avec un modèle local. Si la recherche web est activée dans le script, renseignez la clé demandée dans un fichier `.env` non versionné.

## Exécution

```bash
python chef_personnel_agent.py
```

Les captures présentes dans `images/` illustrent les résultats obtenus, mais la réponse exacte varie selon le modèle.
