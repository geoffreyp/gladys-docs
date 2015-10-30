## AddressToCoordinateService.js 
## AlarmService.js 
## CalendarService.js 
## DistanceService.js 
## GmailService.js 
## GoogleCalendarService.js 
## GoogleContactService.js 
## GoogleMapsService.js 
## HookService.js 
## HouseService.js 
## HttpService.js
## iCalService.js 
## InstallationService.js
## LifeEventService.js
## LocationService.js
## MachineService.js
## MilightService.js



### turnOn (userId,lampId,callback)

* userId : l'ID du User qui déclenche l'action
* lampId: l'ID de la lampe à allumer
* callback : La fonction appelée quand la tâche est terminée

Cette fonction sert à allumer les lampes.

**Utilisation dans un script Gladys**

```
MilightService.turnOn(1, 1);
```

Ce qui allumera la lampe ayant l'ID n°1 dans la base de donnée.


### turnOff (userId,lampId,callback) 

* userId : l'ID du User qui déclenche l'action
* lampId: l'ID de la lampe à allumer
* callback : La fonction appelée quand la tâche est terminée

Cette fonction sert à éteindre les lampes.
**Utilisation dans un script Gladys**

```
MilightService.turnOff(1, 1);
```

Eteindra la lampe ayant l'ID n°1.


### hue (userId,color,callback)

* userId : l'ID du User qui déclenche l'action
* color : Couleur ( entre 0 et 255 )
* callback : La fonction appelée quand la tâche est terminée

Cette fonction modifie la couleur **de la dernière lampe allumée**. 

Utilisation dans un script Gladys :

```
MilightService.hue(1, 80 );
```
Changera la lumière de la dernière ampoule allumée, en vert.


### brightness (userId,brightness,callback)

* userId : l'ID du User qui déclenche l'action
* brightness: Intensité de l'éclairage ( entre 1 et 100 )
* callback : La fonction appelée quand la tâche est terminée

Cette fonction modifie l'intensité **de la dernière lampe allumée**. 

Utilisation dans un script Gladys :

```
MilightService.brightness(1, 50 );
```

Changera l'intensité de la dernière ampoule allumée, à 50.


### effectModeNext (userId,callback)

Cette fonction modifie le mode d'éclairage **de la dernière lampe allumée**. 

Utilisation dans un script Gladys :

```
MilightService.effectModeNext(1);
```

Changera le mode d'éclairage de la dernière ampoule allumée, au mode suivant.


### whiteMode (userId,callback)
* userId: l'ID du User qui déclenche l'action
* callback: La fonction appelée quand la tâche est terminée

Cette fonction modifie le mode d'éclairage **de la dernière lampe allumée**, en mode normal.


**Utilisation dans un script Gladys**

```
MilightService.whiteMode(1);
```
Changera le mode d'éclairage de la dernière ampoule allumée, en mode normal.

## MotionService.js
## MusicService.js
## NotificationService.js
## Oauth2InfosService.js
## PhenixElectricService.js
## pushBulletService.js
## PushoverService.js 
## recommendedSleepTime.js
## RFListenerService.js
## RoomService.js
## ScenarioService.js 
## SchedulerService.js 
## ScriptService.js
## SerialPortService.js
## SocketService.js
## SpeakService.js
## SpeakService.js.BKP
## StartService.js
## SunriseSunsetService.js
## TimerService.js
## UserService.js
## WeatherService.js