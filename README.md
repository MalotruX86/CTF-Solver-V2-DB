# CTF-Solver-V2-DB - Base de données vectorielle

Ce dépôt contient la base de données vectorielle utilisée par [CTF-Solver-V2](https://github.com/MalotruX86/CTF-Solver-V2) - le "Google du PWN" avec analyse par IA.

## Contenu de la base de données

- **4458 write-ups CTF** analysés et indexés
- **66491 chunks vectoriels** pour une recherche sémantique précise
- Couvre toutes les techniques majeures d'exploitation PWN : buffer overflows, ROP, format strings, use-after-free, heap exploitation, shellcoding, etc.
- Base de type Chroma DB optimisée pour la recherche vectorielle
- Compatible avec sentence-transformers pour l'embedding

## Téléchargement

La base de données complète est disponible dans la section [Releases](https://github.com/MalotruX86/CTF-Solver-V2-DB/releases) de ce dépôt.

### Détails techniques
- **Taille** : 268 Mo (compressée en tar.gz)
- **SHA256** : `f2521b665a69fa07bc149fc9d68085143e5f2f9eb0eade590b5763e1aa22bd36`

### Téléchargement

**Lien direct** : [pwn_vector_db.tar.gz (v1.0.0)](https://github.com/MalotruX86/CTF-Solver-V2-DB/releases/download/v1.0.0/pwn_vector_db.tar.gz)

## Installation

Pour l'installer dans votre instance de CTF-Solver-V2 :

```bash
# Créer le répertoire pour la base de données
mkdir -p data/pwn_vector_db

# Télécharger la base de données (~705 Mo)
wget https://github.com/MalotruX86/CTF-Solver-V2-DB/releases/download/v1.0.0/pwn_vector_db.tar.gz

# Extraire l'archive
tar -xzf pwn_vector_db.tar.gz -C data/pwn_vector_db

# Supprimer l'archive après l'extraction (optionnel)
rm pwn_vector_db.tar.gz
```

## Structure de la base de données

La base de données utilise l'architecture ChromaDB et contient :

- Collections d'embeddings
- Métadonnées pour chaque chunk
- Données textuelles sources
- Index optimisés pour la recherche sémantique rapide

## Origine des données

Cette base de données a été créée à l'aide d'un scraper spécialisé dans les write-ups CTF liés au PWN, qui collecte automatiquement et organise les write-ups pour plus de 100 mots-clés liés au PWN à partir de CTFSearch. Les données sont organisées par mot-clé et structurées pour une recherche vectorielle efficace.

## Compatibilité

- Conçue pour fonctionner avec CTF-Solver-V2
- Compatible avec les moteurs de recherche vectorielle basés sur ChromaDB
- Optimisée pour CPU (ne nécessite pas de GPU)

## Licence

Les données sont fournies à des fins éducatives et de recherche uniquement.

## Contribution

Si vous souhaitez contribuer à l'amélioration de cette base de données :

1. Utilisez le script de scraping disponible dans le dépôt principal
2. Analysez et nettoyez vos propres write-ups CTF
3. Soumettez-les via une pull request
