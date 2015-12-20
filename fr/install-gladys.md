Gladys est conçue pour tourner aussi bien sur Linux, Mac ou Windows.

#### Image Raspbian

Pour installer Gladys sur un Raspberry Pi, vous pouvez cloner l'image Raspbian pré-conçue pour Raspberry Pi directement sur votre carte SD ! :)

[<button class="btn btn-success" id="download-raspbian-image">Télécharger Gladys pour Raspberry</button>](https://sourceforge.net/projects/gladys/files/latest/download)

Une fois que vous avez téléchargé le zip :

* Dézipper le fichier zip
* Cloner le fichier .img sur la carte SD ( Suivre les instructions  [ici](https://www.raspberrypi.org/documentation/installation/installing-images/) )
* Insérer la carte SD dans le Raspberry Pi
* Booter sur le raspberry, et au démarrage étendre la partition pour que l'image prenne la taille de votre carte SD. ( voir tutoriel [ici](http://www.soft-alternative.com/raspberry-pi-etendre-partition-systeme-capacite-carte-sd-raspbian.php) )
* C'est tout !

Gladys se lancera automatiquement au démarrage de Raspbian ( Cela peut prendre du temps sur Raspberry Pi B/B+ à se lancer ). Le mot de passe raspbian est toujours le même ( pi:raspberry, et les identifiants MySQL sont root:root ) 

#### Installation manuelle

Pour installer Gladys, il suffit de suivre les instructions sur le [GitHub du projet Gladys](https://github.com/GladysProject/Gladys).