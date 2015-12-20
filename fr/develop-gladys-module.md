En fait un module Gladys n'est ni plus ni moins qu'un Hooks de sails.js ( [Plus d'informations sur les Hooks](https://github.com/balderdashy/sails-docs/blob/master/concepts/extending-sails/Hooks/userhooks.md) ).

Pour vous montrer un example de Hooks, j'ai développé un "ExampleHooks" placé dans le répertoire `api/hooks`. 

Au démarrage de Gladys, ce module effectue plein d'actions :

* Les fichiers dans le dossier "assets" sont copiés dans le répertoire "assets" de l'application mère, pour pouvoir être accessible depuis l'extérieur.
* Les Models sont ajoutés aux modèles de Gladys ( pour pouvoir créer des nouvelles tables dans la base de données )
* Les controllers sont ajoutés aux controllers de Gladys
* Les services sont ajoutés aux services de Gladys et deviennent disponible partout ( même dans les scripts Gladys)
* Les fichiers de config, les policies sont injectés eux aussi à Gladys
* Les widgets de l'écran d'accueil définis dans le fichier `example/lib/parametres.js` sont injectés dans la base de donnée dans la table "DashboardBox" pour être disponible rapidement quand on charge la page d'accueil.

Imaginons que vous vouliez créer un module pour gérer vos lampes connectées, et ainsi rendre Gladys compatible avec votre modèle d'ampoule ! Je vous conseille de procéder ainsi ( c'est un exemple d'implémentation complète de lampes connectées, mais il est possible de créer des modules beaucoup plus simple ) :

* Dupliquez le dossier `api/hooks/example` pour partir d'une base de module qui fonctionne.
* Modifiez le fichier `votre_module/lib/defaults.js`, ainsi que le fichier `votre_module/lib/parametres.js` avec les différentes informations sur votre module.
* Créez un Model sails dans `votre_module/models` pour créer une table pour stocker vos périphériques.
* Créez dans un controller une API REST qui va gérer les interactions avec le client ( ajout/suppression d'un périphérique, allumage/extinction d'une lampe ).
* Créez dans le dossier `assets` un client JS ( une application Angular, ou JQuery, ou pur JS selon vos préférences ) qui va aller demander à l'API les différents périphériques controllable, les injecter dans le widget sur la page d'accueil, et gérer les cliques boutons pour allumer/éteindre les lampes. 
* Modifiez le code HTML du Widget de l'écran d'accueil en touchant au fichier `votre_module/views/box.ejs`.

Pour faire vos tests, vous pouvez directement mettre du code dans le fichier `index.js`, il sera exécuté au chargement de Gladys.
Cependant si vous voulez attendre que Gladys soit bien chargée pour avoir accès à toutes les fonctions de Gladys, placez-vous dans la fonction qui attend l'event "sailsReady" dans le fichier `index.js` :

```
sails.config.Event.on('sailsReady', function(){
     // Est exécuté quand Gladys a fini de charger 
}); 
```