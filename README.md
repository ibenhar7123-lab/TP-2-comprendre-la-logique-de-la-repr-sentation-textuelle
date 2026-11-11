# TP NLP (suite) — Bag of Words et TF-IDF

Suite du TP « Pratique du NLP » : représentation numérique du texte avec scikit-learn.

## Objectifs

- Convertir des phrases en vecteurs avec `CountVectorizer` (Bag of Words)
- Pondérer les mots avec `TfidfVectorizer` (TF-IDF)
- Comparer les deux représentations et en comprendre les limites

## Contenu du projet

| Fichier | Description |
|---|---|
| `TP_NLP_BoW_TFIDF.ipynb` | Notebook avec le code et les réponses aux questions |
| `README_BoW_TFIDF.md` | Ce fichier |

## Structure du notebook

**Préparation** : imports (`pandas`, `scikit-learn`)

**Partie 5 — Bag of Words**
- 5.1 Corpus de 3 phrases (football, cinéma, tennis)
- 5.2 Transformation avec `CountVectorizer`
- 5.3 Vocabulaire extrait
- 5.4 Matrice BoW
- 5.5 Questions (colonnes, limites, perte de l'ordre des mots)

**Partie 6 — TF-IDF**
- 6.1 Transformation avec `TfidfVectorizer`
- 6.2 Matrice TF-IDF
- 6.3 Comparaison BoW / TF-IDF
- 6.4 Poids IDF par mot
- 6.5 Mots les plus importants par phrase
- 6.6 Effet des stopwords
- 6.7 Questions (différence BoW / TF-IDF, mots fréquents, exemple concret)

**Conclusion** : tableau comparatif

## Prérequis

- Python 3.8 ou plus récent
- Jupyter Notebook (inclus dans Anaconda)

## Installation

```bash
pip install scikit-learn pandas
```

## Utilisation

1. Placer les fichiers dans un même dossier.
2. Lancer Jupyter :
   ```bash
   jupyter notebook
   ```
3. Ouvrir `TP_NLP_BoW_TFIDF.ipynb`.
4. Exécuter toutes les cellules : **Kernel → Restart & Run All**.

## Idées clés

- **Bag of Words** : chaque colonne est un mot du vocabulaire, chaque valeur est un nombre d'occurrences. L'ordre des mots est perdu.
- **TF-IDF** : `TF × IDF`. Un mot présent dans beaucoup de documents est pénalisé, un mot rare et distinctif est valorisé.
- Même en TF-IDF, un mot très répété dans un document (comme `the`) peut garder un poids élevé : on retire donc aussi les stopwords (`stop_words="english"`).

## Bibliothèques utilisées

- [scikit-learn](https://scikit-learn.org/) : `CountVectorizer`, `TfidfVectorizer`
- [pandas](https://pandas.pydata.org/) : affichage des matrices sous forme de tableaux
