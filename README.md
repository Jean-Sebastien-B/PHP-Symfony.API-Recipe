Recette perso pour bien cuisiner une API sous Symfony !

Process de création du projet et d'installation des bundles.
  Installation vierge, prête à l'emploi & sans aucune configuration

Prérequis :

Installation de Symfony (sous Windows)

  https://symfony.com/download

Installation de Composer

  https://getcomposer.org/download/

Création du projet :

Open terminal (cmder pour ma part):

`symfony check:requirements`

`symfony new nom-de-votre-api`

`cd nom-de-votre-api`

`composer req symfony/orm-pack`

`composer req --dev symfony/maker-bundle`

`composer req symfony/http:client`

`composer req symfony/security-bundle`

`composer req lexik/jwt-authentication-bundle`

`composer req api`

`symfony serve`ou `php -S localhost:8000 -t public`

Dans le navigateur :

  Accès au projet symfony :
  
    `localhost:8000`

  Accès à la documentation de l'API :
  
    `localhost:8000/api`
    
A ce stade, tout est prêt pour bien commencer. Il ne reste plus qu'à faire tout le reste...

  Configurer le connecteur à la base de données
  
  Créer les entités & leurs relations
  
  Créer la base de données
  
  Gérer la sécurité, l'authentification, les routes... 
  
  Configurer plus finement les ressources exposées (Exposition des ressources & sous-ressources, validation, filtres...)
