##Gladys Node.js API

<div class="alert alert-info" role="alert" style="padding: 10px;">Beware, this documentation is about Gladys 3.0 ! Gladys v2 is going to be deprecated soon, so don't work on it anymore :)</div>

If you are in a script, or in a module, you probably wants to use Gladys functions.

These function are available in the `gladys` variable, which is available everywhere in the code.

### Core

These functions are part of the `core` of Gladys.

To see all parts of the core, see everything [on GitHub](https://github.com/GladysProject/Gladys/tree/v3/api/core).

To take an example, we have the `alarm` folder. It contains all the code related to alarms.

Let's look inside the folder, we have an `index.js` file. This file exposes all alarms functions of the core.

As we can see, it exposes 6 functions :  

```javascript
module.exports.cancel = require('./alarm.cancel.js');
module.exports.create = require('./alarm.create.js');
module.exports.delete = require('./alarm.delete.js');
module.exports.init = require('./alarm.init.js');
module.exports.update = require('./alarm.update.js');
module.exports.schedule = require('./alarm.schedule.js');
```

So, in a script, we can do : 

```javascript
gladys.alarm.cancel(...)
gladys.alarm.create(...)
etc..
```