Projet Triple A — 

Ce projet affiche en temps réel plusieurs informations importantes du système : CPU, mémoire, machine, utilisateurs, et processus.

🖥️ Fonctionnalités
1. Monitoring CPU : 

Nombre de cœurs

Fréquence actuelle

Pourcentage d’utilisation

2. Monitoring Mémoire : 

RAM totale

RAM utilisée

Pourcentage utilisé

3. Informations Système

Nom et OS de la machine

Heure de démarrage

Durée de fonctionnement (uptime)

Nombre d’utilisateurs connectés

Adresse IP principale

4. Processus

Liste des 20 premiers processus classés par utilisation CPU

Liste des 20 premiers processus classés par utilisation RAM

Top 3 des processus les plus gourmands

📂 Organisation du projet : 

monitor.py → script Python qui récupère toutes les informations système

template.html → modèle HTML

template.css → style de la page

index.html → page finale générée automatiquement

README.md → documentation du projet

🔧 Technologies utilisées
Technologie	Rôle
Python	Récupération des données système
psutil	Lecture CPU, RAM, processus
Platform / datetime	Infos machine + date/heure
HTML / CSS	Affichage de la page
Git / GitHub	Versionning + collaboration

Objectif du projet

Créer un tableau de bord simple permettant de visualiser l’état du système à un instant T.

Partie HTML/CSS
Cette partie concerne la création de l’interface web pour afficher les statistiques système collectées par Python.

Points clés

Structure HTML sémantique : <header> avec titre et timestamp, <main> avec cartes (<section class="card">) pour chaque type de données, <footer> pour info de génération.

Variables dynamiques : format {{variable_name}} (snake_case), remplacées par Python.

Disposition et responsive : Grid pour les cartes (2 colonnes desktop, 1 colonne mobile), mobile-first, texte et padding en rem.

Barres de progression et classes d’état :

.status-ok → vert

.status-warning → orange

.status-error → rouge

Les barres et labels changent selon la valeur CPU/RAM.

Palette limitée et contraste suffisant : fond sombre, cartes violettes, accents colorés pour les états.

Lisibilité : unités claires pour RAM, CPU, fichiers.

Interaction avec Python : Python remplit les variables et applique les classes d’état pour afficher l’état correct des jauges.

Résultat : un dashboard clair, structuré, responsive et facile à lire pour évaluer rapidement l’état du système.

