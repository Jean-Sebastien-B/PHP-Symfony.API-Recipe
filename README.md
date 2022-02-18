Recette perso pour bien cuisiner une API sous Symfony !<br>
Certains bundles de cette recette ne sont pas obligatoires et dépendent surtout des besoins :

<i>Le bundle easyadmin n'est utile que si vous désirez un Dashboard pour manipuler aisément vos entités.</br>
Le bundle ldap n'est utile que si vous avez besoin de vous connecter à un ldap ou un AD.</br>
Le bundle psysh n'est utile que si vous appréciez d'effectuer vos requêtes sql de cette manière, au sein d'un terminal.</br>
Le bundle cors n'est utile que si vous envisagez d'installer l'Api & l'IHM sur le même réseau. Règle le problème de 'Cross-Origin Resource Sharing'.</br>
Le bundle jwt n'est utile que si vous préférez gérer l'authentification & vos tokens avec lui plutôt qu'avec le maker, via 'make:auth'.</br></i>


Ce qui suit n'est qu'un process de création de projet & d'installation des bundles que j'utilise le plus fréquemment.<br>
<b>A la fin du process, vous obtenez une installation complète, vierge, prête à l'emploi, mais à ce stade, sans aucune configuration !</b>

Prérequis :

Installation de Symfony (sous Windows)</br>
  `https://symfony.com/download`

Installation de Composer</br>
  `https://getcomposer.org/Composer-Setup.exe`

Création du projet :

Ouvrir votre terminal (<i>cmder pour ma part</i>):<br>
<i>Téléchargeable à cette adresse :</i> https://cmder.net/

`symfony check:requirements` <i>Vérifie que votre environnement est prêt pour créer un projet Symfony...</i><br>
`symfony new nom-de-votre-api` <i>A faire là où vous souhaitez créer votre projet, logiquement, dans votre Workspace...</i><br>
`cd nom-de-votre-api` <i>Vous placer à la racine de votre projet. Là aussi, c'est assez logique !</i><br>

C'est maintenant que tout commence :<br>
`composer req symfony/orm-pack`<br>
  <i>Si vous avez un message concernant le package Zend (utilisé par ocramius) et vous demandant d'installer Laminas</i> :<br>
    Si vous êtes en PHP <7 :<br>
      `composer upgrade`<br>
    Pour les versions >=7 : <br>
      `composer req laminas/laminas-eventmanager`<br>
      `composer req laminas/laminas-code`<br>

`composer req --dev symfony/maker-bundle`<br>
`composer require --dev symfony/profiler-pack`<br>
`composer req psy/psysh:@stable --dev`<br>
`composer req symfony/http-client`<br>
`composer req symfony/http-foundation`<br>
`composer req symfony/security-bundle`<br>
`composer req lexik/jwt-authentication-bundle`<br>
`composer req symfony/ldap`<br>
`composer req api`<br>
`composer req symfony/apache-pack`<br>
`composer req nelmio/cors-bundle`<br>
`composer req easycorp/easyadmin-bundle`

Demarrage du serveur :</br>
`symfony serve`ou `php -S localhost:8000 -t public`

Dans le navigateur :</br>
  Accès au projet symfony :</br>
    `localhost:8000`

  Accès à la documentation de l'API :</br>
    `localhost:8000/api`
    
A ce stade, tout est prêt pour bien commencer. Il ne reste plus qu'à faire tout le reste...</br>
  - Configurer le connecteur à la base de données</br>
  - Créer la base de données</br>
  - Créer les entités & leurs relations</br>
  - Mettre à jour la base de données, via 'doctrine:schema:update --force' directement ou en utilisant les migrations</br>
  - Gérer la sécurité, l'authentification, les routes... </br>
  - Configurer plus finement les ressources exposées (<i>Exposition des ressources & sous-ressources, validation, filtres, Assert...</i>)</br>
  - Et par pitié ! <b>Commentez & documentez votre code</b> !
  ...
