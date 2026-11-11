# Les taxes sur la bière réduisent-elles la mortalité routière ?

Projet personnel de **données de panel** sous R : 48 États américains, 1982-1988 (jeu de données `Fatalities`, package `AER`).

## Résultats clés
- Les comparaisons entre États (coupes transversales, MCO empilés) donnent un effet **positif** de la taxe, ce qui est absurde. C'est un biais d'hétérogénéité non observée.
- Les **effets fixes États** (et les effets fixes États + années) inversent le signe : **−0,66 mort pour 10 000 habitants par dollar de taxe**.
- Le test de **Hausman** rejette les effets aléatoires (p ≈ 2 × 10⁻⁵).
- Les écarts-types sont **robustes par grappe** : le test de Wooldridge détecte une autocorrélation des erreurs.
- Avec des contrôles économiques, l'effet reste négatif (−0,45) mais n'est plus significatif : la preuve est suggestive, pas définitive.
- Bonus : un modèle mixte (ICC = 0,89).

## Fichiers
| Fichier | Contenu |
|---|---|
| `projet_panel_fatalities.html` / `.pdf` | rapport complet : notions, code commenté, sorties, interprétations |
| `projet_panel_fatalities.Rmd` | source R Markdown |
| `Guide_donnees_de_panel.pdf` | guide de méthode : effets fixes, effets aléatoires, modèles mixtes, tests, panels dynamiques |
| `header.tex`, `boxes.lua`, `style.css` | fichiers de mise en forme nécessaires à la compilation |

## Reproduire
R ≥ 4.0, packages `AER`, `plm`, `lmtest`, `sandwich`, `lme4`, `rmarkdown`.

Auteur : Christian TOSSE — M2 Mathématiques des Données, Université Sorbonne Paris Nord.
