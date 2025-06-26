 Projet de site web statique - TMG COLLECTION

Stratégie de branchement
- main: Branche stable finale
- dev: Branche d'intégration
- test/frontend: Branche de test
- feature/*: Branches de développement

Étapes suivies
1. Création de la structure HTML
2. Implémentation du thème CSS
3. Ajout des interactions JavaScript
4. Tests d'intégration
5. Fusion progressive vers dev puis main

Commandes Git utilisées

mkdir

cd

git init

git checkout -b dev

git checkout -b feature/html-structure

git checkout -b feature/css-theme

git checkout -b test/frontend

git checkout feature/html-structure

git add *.html

git commit -m "feat: ajout structure HTML"

git checkout feature/css-theme

git add css/*.css

git commit -m "feat: ajout styles CSS"

git checkout test/frontend

git merge feature/html-structure

git merge feature/css-theme

git checkout dev

git merge test/frontend

git checkout main
git merge dev
