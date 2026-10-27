<div align="center">

# Country Clustering with K-Means

**Grouping 167 countries by socio-economic and health indicators**

<a href="https://colab.research.google.com/github/Steven-Macas/kmeans_paises/blob/main/paises_aprendizaje_automatico_no_supervisado.ipynb"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open in Colab" /></a> <img src="https://img.shields.io/badge/Python-3-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python: 3" /> <img src="https://img.shields.io/badge/Pandas-data-150458?style=flat-square&logo=pandas&logoColor=white" alt="Pandas: data" /> <img src="https://img.shields.io/badge/scikit--learn-ML-F7931E?style=flat-square&logo=scikitlearn&logoColor=white" alt="scikit-learn: ML" /> <img src="https://img.shields.io/badge/Plotly-charts-3F4F75?style=flat-square&logo=plotly&logoColor=white" alt="Plotly: charts" />

</div>

## Overview

Unsupervised learning to group countries according to the factors that determine their level of
development. The result helps identify which countries share similar needs (health, income, trade…).

## Dataset

**Country data** – 167 countries and 9 indicators: child mortality, exports, health spending, imports,
income per person, inflation, life expectancy, fertility rate and GDP per capita.

## Approach

1. Preprocessing and description of each indicator.
2. Correlation matrix, histograms and box plots to spot skewed variables and outliers.
3. Scaling with `StandardScaler`.
4. Cluster stability with jackknife resampling.
5. Choice of the number of groups with the elbow method and the BIC of Gaussian Mixture models.
6. K-Means, evaluated with silhouette and Davies-Bouldin scores.
7. Profiling of every group.

## Results

| Metric (K-Means, k = 4) | Value |
| --- | --- |
| Silhouette score | 0.243 |
| Davies-Bouldin score | 1.24 |

Child mortality separates the groups clearly: from an average of **97.8** deaths per 1,000 births in the
least developed group to **6.7 – 7.2** in the most developed ones.

<table>
  <tr><td align="center" valign="top"><img src="images/correlation.png" alt="Correlation between indicators" width="280" /><br /><sub>Correlation between indicators</sub></td><td align="center" valign="top"><img src="images/boxplots.png" alt="Box plots of the indicators" width="280" /><br /><sub>Box plots of the indicators</sub></td><td align="center" valign="top"><img src="images/bic.png" alt="BIC by number of groups" width="280" /><br /><sub>BIC by number of groups</sub></td></tr>
</table>

## How to run

Open the notebook in Colab with the badge above and upload `Country-data.csv`.

*The notebook is written in Spanish.*

---

<sub>Made by <b>Steven Macas</b> — Data Engineer &amp; Data Analyst · <a href="https://gointy.com">gointy.com</a> · <a href="https://www.linkedin.com/in/steven-macas">LinkedIn</a> · <a href="https://github.com/Steven-Macas">GitHub</a></sub>
