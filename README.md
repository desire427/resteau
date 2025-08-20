# Projet de Gestion de Restaurant - Le Kabouyah

Ce projet est une application web complète pour la gestion d'un restaurant fictif, "Le Kabouyah". Il comprend une vitrine publique pour les clients, un espace client sécurisé et un tableau de bord d'administration pour la gestion interne.

L'application est entièrement développée en utilisant des technologies front-end (HTML, CSS, JavaScript) et simule une base de données en utilisant le `localStorage` du navigateur pour la persistance des données.

## Fonctionnalités

### 1. Site Public (`index.html`)

- **Page d'Accueil :** Présentation attrayante du restaurant.
- **Menu Interactif :** Affichage des plats par catégories (Entrées, Plats, Desserts, Boissons).
  - **Modale de Détails :** Un clic sur un plat ouvre une fenêtre modale avec une image plus grande, la description, le prix et des suggestions de plats similaires.
  - **Bouton "Commander" :** Redirige vers la page de connexion pour commander.
- **Services :** Présentation des services offerts (service à table, événements, livraison, etc.).
- **Formulaire de Réservation Dynamique :**
  - Un clic sur un bouton "Réserver" d'un service fait défiler la page jusqu'au formulaire.
  - Le nom du service est automatiquement affiché dans le formulaire.
  - Le client peut remplir ses informations et envoyer une demande.

### 2. Authentification (`login.html`, `signin.html`, `forgot-password.html`)

- **Inscription :** Les nouveaux clients peuvent créer un compte. Les informations sont sauvegardées localement.
- **Connexion :** Les utilisateurs existants peuvent se connecter. Un système de rôle simple peut être implémenté (par exemple, un email spécifique pour l'admin).
- **Mot de Passe Oublié :** Une page dédiée permet de simuler l'envoi d'un lien de réinitialisation.

### 3. Espace Client (`client.html`)

Un tableau de bord complet pour les clients connectés.

- **Tableau de Bord :** Vue d'ensemble des activités récentes et statistiques personnelles.
- **Mes Informations :** Consultation et modification des informations personnelles (nom, téléphone, etc.).
- **Mes Réservations :**
  - Consultation de l'historique des réservations avec leur statut (En attente, Confirmée, Annulée).
  - Possibilité de faire une nouvelle réservation détaillée.
  - Annulation d'une réservation existante.
- **Mes Commandes :** Historique des commandes (fonctionnalité simulée).
- **Plats Favoris :** Section pour les plats préférés du client (fonctionnalité simulée).
- **Programme Fidélité :** Suivi des points de fidélité et des récompenses (fonctionnalité simulée).
- **Mes Avis :**
  - Consultation des avis déjà soumis avec leur statut (En attente, Publié, Rejeté).
  - **Soumission d'Avis :** Un bouton "Nouvel Avis" ouvre une modale pour rédiger et noter un plat ou un service. L'avis apparaît ensuite dans le tableau avec le statut "En attente".
- **Paramètres :**
  - Gestion des préférences de notification.
  - Changement de mot de passe.
  - Suppression du compte.

### 4. Espace Administrateur (`admin.html`)

Un tableau de bord puissant pour la gestion du restaurant.

- **Tableau de Bord :** Vue d'ensemble des statistiques clés (chiffre d'affaires, réservations, etc.).
- **Gestion des Réservations :**
  - Visualisation de **toutes** les réservations des clients.
  - **Modération :** L'administrateur peut changer le statut d'une réservation pour la "Confirmer" ou l'"Annuler".
- **Gestion du Menu :**
  - **CRUD Complet :** Ajouter, modifier et supprimer des plats du menu.
  - **Upload d'Images :** Association d'une image à chaque plat avec un aperçu dans le formulaire.
  - Les modifications sont sauvegardées et persistantes.
- **Modération des Avis Clients :**
  - Visualisation de tous les avis soumis par les clients.
  - **Actions :** Approuver ("Publier") ou "Rejeter" un avis. Le statut est mis à jour côté client.

## Technologies Utilisées

- **HTML5 :** Pour la structure sémantique des pages.
- **CSS3 :** Pour le style, le design responsive, les animations et l'utilisation de variables.
- **JavaScript (ES6+) :** Pour toute la logique, l'interactivité, la manipulation du DOM et la gestion des données.
- **Font Awesome :** Pour les icônes.
- **Google Fonts :** Pour les polices de caractères (`Montserrat` et `Open Sans`).
- **LocalStorage :** Utilisé comme une base de données simulée pour stocker les utilisateurs, les réservations, le menu et les avis, assurant la persistance des données entre les sessions.

## Installation et Lancement

Ce projet ne nécessite aucune compilation ni dépendance complexe.

1.  Clonez ou téléchargez ce dépôt sur votre machine locale.
    ```sh
    git clone <url-du-repo>
    ```
2.  Naviguez dans le dossier du projet.
3.  Ouvrez le fichier `index.html` directement dans votre navigateur web (Chrome, Firefox, etc.).

> **Recommandation :** Pour une meilleure expérience de développement et pour éviter certains problèmes de sécurité liés au protocole `file://`, il est conseillé d'utiliser une extension de serveur live comme **Live Server** pour Visual Studio Code.

## Comment Utiliser

1.  **Créer un compte client :** Allez sur la page d'accueil (`index.html`), cliquez sur "Espace Client", puis sur le lien "Inscription". Créez un compte.
2.  **Se connecter :** Utilisez les identifiants que vous venez de créer pour vous connecter et accéder à l'espace client (`client.html`).
3.  **Accéder à l'espace admin :** Pour accéder au tableau de bord administrateur, ouvrez directement le fichier `admin.html` dans votre navigateur.

## Structure du Projet

```
restau/
├── admin.html             # Tableau de bord de l'administration
├── client.html            # Espace personnel du client
├── forgot-password.html   # Page de récupération de mot de passe
├── index.html             # Page d'accueil du restaurant
├── login.html             # Page de connexion
├── signin.html            # Page d'inscription
└── README.md              # Ce fichier
```

---

**Auteur :** [POUR KABOUYAH]
