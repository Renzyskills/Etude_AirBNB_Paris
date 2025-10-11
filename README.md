# Etude_AirBNB_Paris
On fera l'analyse , la prédiction, et la visualistion projet (dataset , pris sur kaggle) qui comporte un listing des airbnb de la ville de Pari

---


# Projet : Analyse du dataset Airbnb Paris

**Source :** Kaggle
Lien : [https://www.kaggle.com/datasets/alexmas1991/paris-air-bnb-data-analysis](https://www.kaggle.com/datasets/alexmas1991/paris-air-bnb-data-analysis)

---

### Contexte des données

Les données représentent un listing des différents logements Airbnb situés dans la ville de Paris.
Le jeu de données date de l’année 2018, plus précisément du 6 décembre.

---

### Acteurs concernés

* Les hôtes
* Les voyageurs (clients)
* Le voisinage
* La plateforme Airbnb

---

### But du projet

* **Analyse exploratoire (EDA)** : étudier la répartition des prix, la disponibilité et les évaluations selon les quartiers.
* **Modélisation prédictive** : estimer les prix ou les taux d’occupation à partir des variables fournies.
* **Visualisation géographique** : cartographier la répartition des logements à Paris.

---

### Nombre de variables

18

---

### Analyse EDA

L’analyse exploratoire repose sur un modèle multivarié.

**Objectif :** déterminer la variation du prix en fonction des paramètres suivants :

```
price ↔ availability_365 ↔ reviews_per_month ↔ minimum_nights ↔ room_type ↔ neighbourhood
```

**Signification des principales variables :**

* `availability_365` : disponibilité sur l’année
* `reviews_per_month` : nombre de commentaires ou retours par mois
* `minimum_nights` : nombre minimum de nuits à réserver
* `room_type` : type de bien (appartement, maison, chambre, etc.)
* `neighbourhood` : quartier

---

### Types de graphiques utilisés

#### 1. Boxplot

Utilisé dans deux cas :

* Fluctuation du prix selon le type de logement – Airbnb Paris
* Fluctuation du prix selon le top 10 des quartiers retrouvés le plus fréquemment – Airbnb Paris

Ces graphiques permettent d’observer la dispersion et la médiane des prix selon une catégorie.

**Source du modèle :**
[Matplotlib Boxplot Example](https://matplotlib.org/stable/plot_types/stats/boxplot_plot.html#sphx-glr-plot-types-stats-boxplot-plot-py)

---

#### 2. Scatter / Bubble Plot

Graphique montrant la relation entre le prix, la disponibilité et le type de logement.
Chaque point représente un logement.
La taille du point correspond au nombre de commentaires et la couleur au type de logement.

Ce graphique met en évidence que les logements les plus chers ont souvent une faible disponibilité,
tandis que les logements moins chers sont disponibles plus longtemps.

---

#### 3. Heatmap de répartition (prix ↔ disponibilité)

Cette heatmap montre la densité des logements selon la catégorie de prix et la disponibilité annuelle.
Plus la couleur est foncée, plus le nombre de logements est élevé.

On constate que la majorité des logements se trouvent entre 100 € et 200 €,
avec une disponibilité inférieure à 100 jours,
ce qui reflète une forte demande dans cette gamme tarifaire.

---

#### 4. Heatmap de corrélation (variables numériques)

Cette deuxième heatmap met en évidence la corrélation entre les principales variables numériques :
`price`, `availability_365`, `reviews_per_month`, `minimum_nights` et `number_of_reviews`.

Le graphique montre que le prix est faiblement corrélé aux autres variables,
ce qui signifie que le tarif dépend surtout de facteurs qualitatifs
comme le type de logement ou la localisation.

On remarque aussi une corrélation modérée entre `reviews_per_month` et `number_of_reviews` (environ 0.55),
ce qui est logique : plus un logement reçoit d’avis, plus il en reçoit chaque mois.

---

### Remarques générales

* Les logements les plus chers sont souvent des appartements entiers ou des hôtels.
* Les chambres privées affichent généralement les prix les plus bas.
* Les logements les plus demandés sont aussi les moins disponibles (entre 0 et 100 jours par an).
* Les variables numériques telles que `availability_365`, `minimum_nights` et `reviews_per_month`
  ont peu d’influence directe sur le prix.

---

### Outils utilisés

* Python 3.13
* Pandas, NumPy, Matplotlib, Seaborn
* Jupyter Notebook (VS Code)

---

### Conclusion

Cette analyse EDA permet de mieux comprendre le marché Airbnb parisien.
Les prix varient principalement selon le type de logement et le quartier,
tandis que la disponibilité et les avis ont un impact moindre.

Les résultats de cette étude serviront de base à la phase suivante du projet,
notamment la modélisation prédictive et la visualisation des données sur Power BI.

---


