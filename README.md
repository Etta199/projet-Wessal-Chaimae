# projet-Wessal-Chaimae
# Webapp de DataScience avec Flask
Webapp de science des données pour montrer certaines des capacités de Flask et des bibliothèques telles que sklearn, pandas, matplotlib, seaborn...

## Capacités :

### Téléchargement de données
La webapp supporte :
- CSV (délimiteur : ',')
- TXT (délimiteur : tab)

### Résumé du jeu de données
Cette page affichera :
- 5 premières lignes pour voir l'aspect général de l'ensemble de données.
- Un résumé statistique de chaque colonne.

### Prétraitement
Nous pouvons créer un nouveau jeu de données (il sera enregistré au format CSV) avec les options suivantes :

Sélection des caractéristiques :
- Sélection automatique basée sur l'estimateur du Khi-deux (le nom sera créé en fonction des paramètres choisis) :
  - Nombre de caractéristiques
  - Variable de réponse
- Sélection manuelle :
  - Nom du nouvel ensemble de données
  - Sélection des variables

Valeurs nulles et colonnes avec une valeur unique :
- Supprimer les lignes avec des valeurs nulles :
  - Nulle dans TOUTES les colonnes
  - Nulle dans TOUTES les colonnes
  - Jamais
- Suppression des variables ayant une valeur unique :
  - Oui
  - Non
  
* Un prétraitement supplémentaire (normalisation, variables fictives...) sera effectué dans les étapes de modélisation et de prédiction.

### Graphiques
Visualisations disponibles pour les variables choisies :

- Histogrammes
- BoxPlots
- Graphiques de corrélation

### Modèles
Modèles pour les tâches de classification et de régression.
Il ne supporte pas la classification multiclasse pour le moment (code supplémentaire pour gérer certaines métriques et graphiques).

Algorithmes disponibles :
- Régression logistique (Classification)
- Régression linéaire (Régression)
- Random Forests (les deux)
- K plus proches voisins (les deux)
- AdaBoost (les deux)
- Extreme Gradient Boosting (les deux)
- Perceptron multicouche (les deux)

Validation croisée K-Fold (3, 5, 10)

Mise à l'échelle standard (Oui, Non)

Sélection manuelle des caractéristiques

Tâches de classification Sortie :
- Temps d'ajustement
- Temps de score
- Précision (Test et Train)
- Rappel (Test et Train)
- Score F1 (Test et Train)
- Exactitude (Test et Train)
- AUC ROC (Test et Train)
- Tracé des courbes ROC

Tâches de régression Sortie :
- Temps d'ajustement
- Temps de score
- Variance expliquée (Test et Train)
- R2 (Test et Train)
- Erreur quadratique moyenne (Test et Train)
- Tracé des valeurs mesurées par rapport aux valeurs prédites

### Prédictions
Construction du modèle (avec l'ensemble complet de données) et prédiction pour un ensemble de valeurs introduites.
Le modèle n'inclura que les variables avec une valeur introduite.
Les algorithmes disponibles sont les mêmes que ceux mentionnés dans "Modèles".
Il supporte également les problèmes multi-classes.
