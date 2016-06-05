##Writing a Gladys script

<div class="alert alert-info" role="alert" style="padding: 10px;">Beware, this documentation is about Gladys 3.0 ! Gladys v2 is going to be deprecated soon, so don't work on it anymore :)</div>

Scripts in Gladys allows you to write little JavaScript programs with access to the full API of Gladys.

### Sandbox

Scripts are running in a sandbox, you don't have access to the full Node.js native API ( like `require` for example ). You can only call Gladys functions.

### Available functions

You call all Gladys functions, and all function exposed by modules.

For example, all the functions of the modules 'MODULE_NAME' are available in the following object :  

```javascript
gladys.modules.MODULE_NAME
```

So, if the module 'test' has a `getWeather()` function, you can do :

```javascript
gladys.modules.test.getWeather();
```