# projet-metaheuristique

# 🌍 Optimisation par Essaim Particulaire (PSO) pour le Problème du Voyageur de Commerce (TSP)


Ce dépôt contient le code source, les jeux de données et le rapport complet de mon projet universitaire portant sur la résolution du **Problème du Voyageur de Commerce (TSP - Traveling Salesman Problem)** à l'aide de l'algorithme d'**Optimisation par Essaim Particulaire (PSO)**.

Projet réalisé dans le cadre de mon cursus à la **Faculté des Sciences de Meknès (Université Moulay Ismail)**.

---

## 🎯 Objectifs du Projet

L'objectif principal est de concevoir, implémenter et évaluer une métaheuristique (PSO) capable d'améliorer une solution initiale générée par une heuristique classique (Glouton) sur des instances réelles du TSP.

### Approches implémentées :
1. **Heuristique Gloutonne (Nearest Neighbor) :** Méthode constructive rapide ($O(N^2)$) servant de base de référence.
2. **PSO "Cold Start" :** Implémentation standard du PSO avec initialisation aléatoire des particules.
3. **PSO "Warm Start" :** Injection de la solution gloutonne dans l'essaim initial pour guider la recherche.
4. **PSO Hybride Amélioré (PSO + 2-opt + Restart) 🏆 :** La version finale de l'algorithme qui combine l'exploration globale du PSO, l'intensification locale de l'opérateur *2-opt*, et une stratégie de *restart* pour éviter les optima locaux.

---

## 📂 Structure du Dépôt

- `projet_metaheuristique.ipynb` : Le notebook Jupyter contenant l'intégralité du code (chargement des données, algorithmes, affichage des cartes et des graphiques de convergence).
- `Rady_hassane.pdf` : Le rapport de projet détaillé (formulation mathématique, méthodologie, analyse des résultats et conclusion).
- `[Dossier des instances]` : Contient les 14 fichiers d'instances de test issues de la bibliothèque **TSPLIB** (de 48 à 2152 villes, ex: `att48`, `berlin52`, `u2152`).

---

## 📊 Résultats Clés et Performances

Les algorithmes ont été testés sur 14 instances de tailles croissantes. L'algorithme **PSO Hybride** a démontré une supériorité claire par rapport aux autres méthodes :

* **Gain de Qualité :** Une réduction de la distance totale allant de **5% à plus de 16%** par rapport à la méthode gloutonne.
* **Compromis Temps/Qualité :** Bien que le PSO hybride soit plus coûteux en temps de calcul (en raison des itérations de la recherche locale 2-opt), ce surcoût est largement justifié par les gains substantiels obtenus sur la distance finale.

*(Pour voir les tableaux statistiques complets et les courbes de convergence, n'hésitez pas à consulter le fichier PDF `Rady_hassane.pdf`).*

---

## 🛠️ Comment exécuter le projet ?

### Prérequis
Assurez-vous d'avoir Python installé ainsi que les bibliothèques suivantes :
```bash
pip install numpy pandas matplotlib scipy
