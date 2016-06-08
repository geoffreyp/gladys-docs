### Action 

- `post /action`
- `delete /action/:id`
- `patch /action/:id`
- `post /action/:id/param`  
  
###ActionParam
 
- `patch /actionparam/:id`
  
###ActionType

- `get /actiontype`
- `get /actiontype/:id/params`
  
### Alarm

- `get /alarm`: `AlarmController.index`,
- `post /alarm`: `AlarmController.create`,
- `post /alarm/timer`: `AlarmController.timer`,
- `delete /alarm/:id`: `AlarmController.delete`,
  
### Area

- `get /area`: `AreaController.index`,
- `post /area`: `AreaController.create`,
- `patch /area/:id`: `AreaController.update`,
- `delete /area/:id`: `AreaController.delete`,
  
### Box

- `get /box`: `BoxController.index`,
- `post /box`: `BoxController.create`,
- `delete /box/:id`: `BoxController.delete`,
  
###BoxType

- `get /boxtype` : `BoxTypeController.index`,
  
### Brain

- `get /brain/classify`: `BrainController.classify`, 
- `post /brain/trainnew`: `BrainController.trainNew`, 
  
  
###Category

- `get /category`: `CategoryController.index`,
- `get /category/:service/eventtype`: `CategoryController.getEventTypes`,
  
### Device 

- `get /device`: `DeviceController.index`,
- `post /device`: `DeviceController.create`,
- `patch /device/:id`: `DeviceController.update`,
- `delete /device/:id`: `DeviceController.delete`,
- `get /device/:id/devicetype`: `DeviceController.getDeviceTypes`,
  
  
### DeviceState
 
- `get /devicestate`: `DeviceStateController.index`,
  
### DeviceType

- `get /devicetype`: `DeviceTypeController.index`
- `get /devicetype/room`: `DeviceTypeController.getByRoom`,
- `patch /devicetype/:id`: `DeviceTypeController.update`,
- `post /devicetype/:id/exec`: `DeviceTypeController.exec`,
  
### Event

- `get /event`: `EventController.index`,
- `post /event`: `EventController.create`,
- `get /event/create`: `EventController.create`,

  
###EventType

- `get /eventtype`: `EventTypeController.index`,
- `get /eventtype/:id/launcherparam`: `EventTypeController.getLauncherParams`,
  
### House

- `get /house`: `HouseController.index`,
- `post /house`: `HouseController.create`,
- `patch /house/:id`: `HouseController.update`,
- `delete /house/:id`: `HouseController.delete`,
- `get /house/:id/user`: `HouseController.getUsers`,
  
### Launcher

- `get /launcher`: `LauncherController.index`,
- `post /launcher`: `LauncherController.create`,
- `patch /launcher/:id`: `LauncherController.update`,
- `delete /launcher/:id`: `LauncherController.delete`,
- `get /launcher/:id/action`: `LauncherController.getActions`,
`get /launcher/:id/state`: `LauncherController.getStates`,

### Location

- `post /location`: `LocationController.create`,
- `get /location/create`: `LocationController.create`,
  
### Mode

- `get /mode`: `ModeController.index`,
- `post /mode`: `ModeController.create`,
- `delete /mode/:id`: `ModeController.delete`,
- `post /house/:id/mode`: `ModeController.change`, 
  
### Module

- `get /module`: `ModuleController.index`,
- `post /module/install`: `ModuleController.install`,
- `post /module/:slug/config`: `ModuleController.config`,
- `delete /module/:id`: `ModuleController.uninstall`,
  
### Notification

- `get /notification`: `NotificationController.index`,
  
### NotificationType

- `get /notificationtype`: `NotificationTypeController.index`,
  
### NotificationUser

- `get /notificationuser`: `NotificationUserController.index`,
- `post /notificationuser`: `NotificationUserController.create`,
- `patch /notificationuser/:id`: `NotificationUserController.update`,
- `delete /notificationuser/:id`: `NotificationUserController.delete`,
  
### Param

- `get /param`: `ParamController.index`,
- `post /param`: `ParamController.create`,
- `patch /param/:name`: `ParamController.update`,
- `delete /param/:name`: `ParamController.delete`,
  
### ParamUser

- `get /paramuser`: `ParamUserController.index`,
- `post /paramuser`: `ParamUserController.create`,
- `patch /paramuser/:name`: `ParamUserController.update`,
- `delete /paramuser/:name`: `ParamUserController.delete`,
  
### Script

- `get /script`: `ScriptController.index`,
- `post /script`: `ScriptController.create`,
- `patch /script/:id`: `ScriptController.update`,
- `post /script/:id/exec`: `ScriptController.exec`,
- `delete /script/:id`: `ScriptController.delete`,
  
### Room

- `get /room`: `RoomController.index`,
- `post /room`: `RoomController.create`,
- `patch /room/:id`: `RoomController.update`,
- `delete /room/:id`: `RoomController.delete`,
  
###Socket

- `post /socket/subscribe`: `SocketController.subscribe`,
  
### State

- `post /state`: `StateController.create`,
- `patch /state/:id`: `StateController.update`,
- `delete /state/:id`: `StateController.delete`,
- `post /state/:id/param`: `StateController.addParam`,
  
### StateType

- `get /statetype`: `StateTypeController.index`,
- `get /statetype/:id/param`: `StateTypeController.getStateTypeParams`,
- `get /statetype/:id/templateparam`: `StateTypeController.getTemplateParams`,
  
  
### System

- `get /system`: `SystemController.index`,
- `post /system/shutdown`: `SystemController.shutdown`,
  
### Token

- `get /token`: `TokenController.index`,
- `post /token`: `TokenController.create`,
- `patch /token/:id`: `TokenController.update`,
- `delete /token/:id`: `TokenController.delete`,
  
  
### Update

- `get /update/verify`: `UpdateController.verify`,
- `get /update/event`: `UpdateController.updateEvents`,
- `get /update/mode`: `UpdateController.updateModes`,
- `get /update/sentence`: `UpdateController.updateSentences`,
- `get /update/box`: `UpdateController.updateBoxTypes`,
- `get /update/category`: `UpdateController.updateCategories`,
- `get /update/state`: `UpdateController.updateStates`,
  
###User

- `get /user`: `UserController.index`,
- `post /user`: `UserController.create`,
- `post /user/login`: `UserController.login`,
- `patch /user/:id`: `UserController.update`,
- `delete /user/:id`: `UserController.delete`,
- `get /user/whoami`: `UserController.whoami`,