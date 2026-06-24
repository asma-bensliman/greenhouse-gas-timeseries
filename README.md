# Analyse de séries temporelles — Gaz à effet de serre 🌍

Étude statistique de l'évolution de quatre gaz à effet de serre (**CO₂, CH₄, N₂O, SF₆**) à partir de relevés mensuels du [Global Monitoring Laboratory](https://gml.noaa.gov/) (NOAA). Projet réalisé en **Python** dans un Notebook Jupyter, dans le cadre du cours de statistiques (2STAT) à SUPINFO.

## 👥 Auteures

Projet réalisé **en binôme** :

- **Asma Ben Sliman** — [github.com/asma-bensliman](https://github.com/asma-bensliman)
- **Paola** ⚠️ *(ajouter nom complet / lien GitHub)*

## 🎯 Objectif

Décrire et modéliser l'évolution des émissions de chaque gaz, distinguer les gaz à **forte saisonnalité** de ceux à tendance régulière, puis produire des **prévisions sur 2 ans**.

## 🧰 Stack technique

- **Python** — Pandas, NumPy
- **Visualisation** — Matplotlib
- **Modélisation** — scikit-learn (régression linéaire, `r2_score`)
- **Format** — Jupyter Notebook

## 📊 Démarche

1. **Chargement & nettoyage** des 4 jeux de données (sélection des variables `month` et `average`, période et nombre d'observations)
2. **Présentation des gaz** étudiés : formule chimique, effets sur l'atmosphère, unité de mesure
3. **Visualisation** par nuages de points et identification des gaz à variations saisonnières
4. **Décomposition saisonnière** (gaz saisonniers) :
   - Moyenne mobile d'ordre 6 → **série lissée**
   - Coefficients mensuels et coefficients **corrigés**
   - **Série corrigée des variations saisonnières (CVS)**
   - Modèles **additif** et **multiplicatif**, puis comparaison
   - **Tendance** (droite de régression) et **prévisions** à 2 ans
5. **Régression** (gaz non saisonniers) : coefficient de corrélation, droites de régression **linéaire** et **exponentielle**, prévisions
6. **Agrégation annuelle** et régression sur les moyennes par année

## 📁 Contenu du dépôt

| Fichier | Description |
|---|---|
| `projet.ipynb` | Notebook complet (code, graphiques, interprétations) |
| `projet.html` | Export HTML du notebook (lecture sans exécution) |
| `co2_mm_mlo.csv` | CO₂ — Mauna Loa, mensuel |
| `ch4_mm_gl.csv` | CH₄ — moyenne globale, mensuel |
| `n2o_mm_gl.csv` | N₂O — moyenne globale, mensuel |
| `sf6_mm_gl.csv` | SF₆ — moyenne globale, mensuel |

> Données : Global Monitoring Laboratory (NOAA) — domaine public.

## ▶️ Exécution

```bash
pip install pandas numpy matplotlib scikit-learn jupyter
jupyter notebook projet.ipynb
```

Ou ouvrir directement `projet.html` dans un navigateur pour consulter les résultats.
