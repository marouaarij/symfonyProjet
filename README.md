<<<<<<< HEAD
---

##Journal de développement (Étapes réalisées)


### Phase 1 : Préparation de l'environnement (WSL)
* **Diagnostic :** Problème de dépendances PHP détecté lors de l'utilisation de Composer.
* **Action :** Installation des extensions manquantes sur Ubuntu.
* `sudo apt install php-xml php-zip php-mbstring unzip`

### Phase 2 : Initialisation du Projet
* **Organisation :** Création d'un répertoire de travail dédié pour éviter les conflits de permissions.
* `mkdir ~/mes_projets`
* **Création :** Génération du squelette Symfony avec l'option Webapp (MVC complet).
* `symfony new tp3_symfony --webapp`

### Phase 3 : Développement MVC
Mise en place des trois composants du pattern MVC :
1.  **Modèle (Formulaire) :** Génération du FormType pour gérer la quantité et la couleur.
* `php bin/console make:form AddToCartType`
2.  **Contrôleur :** Création de la logique métier et de la route `/product`.
* `php bin/console make:controller ProductController`
3.  **Vue :** Intégration de Bootstrap 5 dans le template Twig.
* Fichier : `templates/product/index.html.twig`

### Phase 4 : Debugging & Configuration
Résolution d'un problème de routage majeur (Erreur 404 sur `/product`).
* **Analyse :** La commande `php bin/console debug:router` ne listait pas la nouvelle route.
* **Correctif :**
1.  Configuration du fichier `config/routes.yaml` pour activer le scan des annotations (Attributes).
2.  Vidage du cache de développement.
* `php bin/console cache:clear`

### Phase 5 : Déploiement Git
* **Versionning :** Initialisation du dépôt local.
* **Liaison Remote :** Connexion au dépôt GitHub.
* `git remote add origin https://github.com/4AT9/tp3_symfony.git
* **Push :** Envoi sécurisé des sources.
* `git push -u origin main`
=======
# symfonyProjet
>>>>>>> fec1f20043cf6d1f5d4e5e2e521289c08fa97cb3
