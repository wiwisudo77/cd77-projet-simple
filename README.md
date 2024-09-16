# cd77-projet-simple
Objectif du projet

1 - Configurer un dépôt GitLab avec un projet simple.
2 - Mettre en place un pipeline d'intégration continue (CI) pour construire et tester le projet.
3 - Configurer le déploiement continu (CD) pour déployer automatiquement le projet.

Etape 1 : Création du projet GitLab

  * Créer un nouveau projet sur GitLab (intégration <prenom>-ci)
  * Cloner le dépôt sur votre machine locale
  * Vérifier la configuration de votre projet afin de pouvoir pousser et tirer depuis votre dépot

Etape 2 : Configuration de l'intégration continue (CI)

  * Créer un fichier de configuration .gitlab-ci.yml (branche developpement)
  * Créer un pipeline permettant de tester l'application en utilisant l'image docker python:3.9 (pour tester l'application utiliser la commande python app.py)
  * Vérifier que votre pipeline s'exécute sans erreur

Etape 3 : Configuration du déploiement continu (CD)

  * Depuis votre poste, mettre à jour le fichier .gitlab-ci.yml pour inclure les étapes de déploiement (ne devra être executé manuellement que sur la branche production)
  * Pousser les modifications vers GitLab
  * Vérifier le déploiement
    
NB : pour le déploiement utiliser les commandes
* docker build -t <prenom> . "Pour construire l'image correspondant à votre application"
* docker run -d -p 5000:5000 <prenom> "Pour démarrer un conteneur exécutant l'image précédente"
