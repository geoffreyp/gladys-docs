## Installer Gladys

<div class="alert alert-info" role="alert" style="padding: 10px;">Attention, cette documentation explique comment installer Gladys en mode développeur pour la v3 ! La version 2 étant bientôt deprecated, inutile de développer pour la v2 ! Cette installation est conçue pour développer, ce n'est pas comme cela qu'on installe Gladys en production.</div>


Gladys est conçue pour tourner aussi bien sur Linux, Mac ou Windows.
Nous allons voir ici comment installer Gladys en tant que développeur depuis le github.

### Pré-requis

- Node.js >= 4.2.2 ( pas compatible avec Node.js v5 )
- MySQL
- Command Line Tools
 - <img src="https://developer.gladysproject.com/assets/images/documentation/apple.gif" height="17">&nbsp;**Mac OS X**: [Xcode](https://itunes.apple.com/us/app/xcode/id497799835?mt=12) (or **OS X 10.9 Mavericks**: `xcode-select --install`)
 - <img src="https://developer.gladysproject.com/assets/images/documentation/windows.jpg" height="17">&nbsp;**Windows**: [Visual Studio](http://www.visualstudio.com/downloads/download-visual-studio-vs#d-express-windows-8)
 - <img src="https://developer.gladysproject.com/assets/images/documentation/ubuntu.jpg" height="17">&nbsp;**Ubuntu**, **Debian**: `sudo apt-get install build-essential`

### Cloner Gladys

Tout d'abord, on clone Gladys.

```
git clone https://github.com/GladysProject/Gladys.git gladys
```

On se met dans le dossier gladys, puis on se place sur la branche de développement :

```
cd gladys && git checkout v3
```


### Installer les dépendances

On exécute la commande suivante toujours dans le dossier gladys : 

```
sudo npm install && npm install -g sails && npm install -g grunt-cli
``` 

**Note :** Le sudo n'est pas obligatoire, cela dépend de votre système et de vos droits. A mettre selon votre usage habituel de Node.js.

### Définir les variables d'environnements

Afin que Gladys puisse se connecter à MySQL, vous devez définir plusieurs variables d'environnements: 

`MYSQL_HOST`, `MYSQL_PORT`, `MYSQL_USER`, `MYSQL_PASSWORD` et `MYSQL_DATABASE`.

Placez dans ces variables d'environnements les bonnes valeurs pour votre configuration de MySQL.

Si vous ne savez pas comment modifier des variables d'environnements, il y a des centaines de tutos sur Google pour tous les systèmes ;)

**La méthode dirty:**

Si vous n'arrivez vraiment pas à modifier les variables d'environnements, vous pouvez modifier le fichier `config/connections.js`.


### Lancer Gladys en mode développement

Pour lancer Gladys en mode développement, vous n'avez qu'à faire dans le dossier Gladys :

```
sails lift
```

Vous pouvez désormais accéder à Gladys sur l'URL suivante :

```
http://localhost:1337
```

### Lancer Gladys en mode production


Tout d'abord on compile les assets et on initialise Gladys :

```
node init.js && grunt buildProd
```

Enfin, on lance Gladys en production :

```
node app.js
```

Vous pouvez désormais accéder à Gladys sur l'URL suivante :

```
http://localhost:8080
```


### Lancer les tests unitaires

Pour lancer les tests unitaires, vous pouvez lancer la commande : 

```
grunt coverage
```
