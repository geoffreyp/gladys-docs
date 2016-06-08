### Action 

- `post /action`

**Post data:**

```json
{
	"action": 1,
	"launcher": 1
}
```

- `delete /action/:id`
- `patch /action/:id`
- `post /action/:id/param`  

**Post data:**

```json
{
	"value": 10,
	"action": 1,
	"actiontypeparam": 1
}
```
  
###ActionParam
 
- `patch /actionparam/:id`
  
###ActionType

- `get /actiontype`
- `get /actiontype/:id/params`
  
### Alarm

- `get /alarm` 
- `post /alarm`

**Post data:**

```json
{
    "name": "Alarm ",
    "dayofweek": 1,
    "time": "13:01",
    "user": 1
  }
```
- `post /alarm/timer`:

**Post data:**

```json
{
	"name": "This is a cool timer",
    "duration": 60, // seconds
    "user": 1
}
```

- `delete /alarm/:id`: `AlarmController.delete`,
  
### Area

- `get /area`
- `post /area`

**Post data:**

```json
{
    "id": 1,
    "name": "My Gorgeous House",
    "latitude": 40.7412,
    "longitude": -73.9896,
    "radius": 100,
    "user": 1
}
```

- `patch /area/:id`
- `delete /area/:id`
  
### Box

- `get /box`
- `post /box`
- `delete /box/:id`
  
###BoxType

- `get /boxtype`
  
### Brain

- `get /brain/classify` 
- `post /brain/trainnew`
  
###Category

- `get /category`
- `get /category/:service/eventtype`
  
### Device 

- `get /device`
- `post /device`

**Post data:**

```json
{
	"id": 1,
	"name": "Switch",
	"protocol": "zwave",
	"service": "zwave",
	"room": 1
}
```

- `patch /device/:id`
- `delete /device/:id`
- `get /device/:id/devicetype`
  
### DeviceState
 
- `get /devicestate`
  
### DeviceType

- `get /devicetype`
- `get /devicetype/room`
- `patch /devicetype/:id`
- `post /devicetype/:id/exec`
  
### Event

- `get /event`
- `post /event`

**Post data:**

```json
{
    "id": 1,
    "eventtype": 1,
    "datetime": "2015-05-12 18:00:00",
    "user": 1
}
```
   
- `get /event/create`

**Get data:** Same as post.
  
###EventType

- `get /eventtype`
- `get /eventtype/:id/launcherparam`
  
### House

- `get /house`
- `post /house`

**Post data:**

```json
{
    "id": 1,  
    "uuid": "2094b316-c295-48d7-bbdd-40360d2543dd",
    "name": "My house",
    "address": "102 avenue des Champs-Elysées",
    "city" : "Paris",
    "postcode" : "75008",
    "country": "France",
    "latitude": 37.773972,
    "longitude": -122.431297
 }
```

- `patch /house/:id`
- `delete /house/:id`
- `get /house/:id/user`
  
### Launcher

- `get /launcher`
- `post /launcher`
- `patch /launcher/:id`
- `delete /launcher/:id`
- `get /launcher/:id/action`
- `get /launcher/:id/state`

### Location

- `post /location`

**Post data:**

```json
{
    "id": 1,
    "user": 1,
    "latitude": 40.7412,
    "longitude": -73.9896,
    "datetime": "2015-05-12 18:00:00"
}
```

- `get /location/create`

**Get data:** Same as post.
  
### Mode

- `get /mode`
- `post /mode`
 
**Post data:**

```json
{
    "id": 1,
    "code": "at-home",
    "name": "At home",
    "description": "You are at home"
}
```

- `delete /mode/:id`
- `post /house/:id/mode`

**Post data:**

```json
{
    "mode": "at-home"
}
```
  
### Module

- `get /module`
- `post /module/install`
- `post /module/:slug/config`
- `delete /module/:id`
  
### Notification

- `get /notification`
  
### NotificationType

- `get /notificationtype`
  
### NotificationUser

- `get /notificationuser`
- `post /notificationuser`
- `patch /notificationuser/:id`
- `delete /notificationuser/:id`
  
### Param

- `get /param`
- `post /param`
- `patch /param/:name`
- `delete /param/:name`
  
### ParamUser

- `get /paramuser`
- `post /paramuser`
- `patch /paramuser/:name`
- `delete /paramuser/:name`
  
### Script

- `get /script`
- `post /script`
- `patch /script/:id`
- `post /script/:id/exec`
- `delete /script/:id`
  
### Room

- `get /room`
- `post /room`
- `patch /room/:id`
- `delete /room/:id`
  
###Socket

- `post /socket/subscribe`
  
### State

- `post /state`
- `patch /state/:id`
- `delete /state/:id`
- `post /state/:id/param`
  
### StateType

- `get /statetype`
- `get /statetype/:id/param`
- `get /statetype/:id/templateparam`
  
  
### System

- `get /system`
- `post /system/shutdown`
  
### Token

- `get /token`
- `post /token`
- `patch /token/:id`
- `delete /token/:id`
  
  
### Update

- `get /update/verify`
- `get /update/event`
- `get /update/mode`
- `get /update/sentence`
- `get /update/box`
- `get /update/category`
- `get /update/state`
  
###User

- `get /user`
- `post /user`
- `post /user/login`
- `patch /user/:id`
- `delete /user/:id`
- `get /user/whoami`