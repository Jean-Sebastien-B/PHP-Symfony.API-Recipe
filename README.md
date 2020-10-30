Recette perso pour bien cuisiner une API sous Symfony !
Certains bundles de cette recette ne sont pas obligatoires et dépendent surtout des besoins :

Le bundle easyadmin n'est utile que si vous désirez un Dashboard pour manipuler aisément vos entités.
Le bundle ldap n'est utile que si vous avez besoin de vous connecter à un ldap ou un AD.
Le bundle psysh n'est utile que si vous appréciez d'effectuer vos requêtes sql de cette manière, au sein d'un terminal. 

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

`composer req psy/psysh:@stable --dev`

`composer req symfony/http:client`

`composer req symfony/http:foundation`

`composer req symfony/security-bundle`

`composer req lexik/jwt-authentication-bundle`

`composer req symfony/ldap`

`composer req api`

`composer req symfony/apache-pack`

`composer req easycorp/easyadmin-bundle`

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
  
  ...
