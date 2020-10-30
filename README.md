Recette perso pour bien cuisiner une API sous Symfony !<br>
Certains bundles de cette recette ne sont pas obligatoires et dépendent surtout des besoins :

<i>Le bundle easyadmin n'est utile que si vous désirez un Dashboard pour manipuler aisément vos entités.

Le bundle ldap n'est utile que si vous avez besoin de vous connecter à un ldap ou un AD.

Le bundle psysh n'est utile que si vous appréciez d'effectuer vos requêtes sql de cette manière, au sein d'un terminal. </i>


Ce qui suit n'est qu'un process de création de projet & d'installation des bundles que j'utilise le plus fréquemment.<br>
<u>A la fin du process, vous obtenez une installation complète, vierge, prête à l'emploi, mais à ce stade, sans aucune configuration !</u>

Prérequis :

Installation de Symfony (sous Windows)

  https://symfony.com/download

Installation de Composer

  https://getcomposer.org/download/

Création du projet :

Open terminal (cmder pour ma part):

`symfony check:requirements`<br>
`symfony new nom-de-votre-api`<br>
`cd nom-de-votre-api`<br>
`composer req symfony/orm-pack`<br>
`composer req --dev symfony/maker-bundle`<br>
`composer req psy/psysh:@stable --dev`<br>
`composer req symfony/http:client`<br>
`composer req symfony/http:foundation`<br>
`composer req symfony/security-bundle`<br>
`composer req lexik/jwt-authentication-bundle`<br>
`composer req symfony/ldap`<br>
`composer req api`<br>
`composer req symfony/apache-pack`<br>
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
