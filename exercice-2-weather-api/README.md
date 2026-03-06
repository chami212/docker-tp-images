# Exercice 2 - API Node.js optimisee et publiee

Objectif: dockeriser une API Node.js, optimiser le build et publier l'image sur Docker Hub.

## Contexte

Tu disposes d'une API meteo Express qui expose:
- `GET /api/weather/:city`
- `GET /health`

## Fichiers du projet

- `index.js`
- `package.json`

## Travail a faire

1. Creer un `.dockerignore` pour exclure les fichiers inutiles du contexte de build.

2. Creer un `Dockerfile` optimise qui:
- utilise `node:18-alpine`
- copie d'abord `package.json`
- installe les dependances
- copie ensuite le reste du code
- expose le port `3000`
- lance l'application

3. Construire une image taggee avec ton username Docker Hub:
- `tonusername/weather-api:1.0.0`

4. Tester l'application localement:
- endpoint meteo sur `/api/weather/paris` OK
- endpoint sante sur `/health` OK

5. Publier l'image sur Docker Hub puis creer/publier le tag `latest`.

6. Verifier que le repository Docker Hub est public et contient bien les deux tags. OK

Les commandes doivent etre fournies dans un fichier separe `COMMANDS.md`.

## Questions de reflexion

- Pourquoi copier `package.json` avant le reste du code ?
pour pouvoir utiliser le cache de docker si package.json ne change pas, docker ne réinstalle pas les dépendances et réutilise la couche déjà construite
- Quelle difference de taille entre `node:18` et `node:18-alpine` ?
node:18 équivaut à, à peu près 1Gb et la version alpine 170mb donc plus minimal
- A quoi sert le tag `latest` ?
permettre d'utiliser la derniere version d'une image si elle est postée si on pull une image sans lui donner de version elle prendra celle liée à latest, la derniere

## Criteres de validation

- L'image finale fait moins de 150 MB
- L'API repond correctement sur `/api/weather/paris`
- L'image est visible sur Docker Hub: `tonusername/weather-api`
- Les tags `1.0.0` et `latest` sont presents
