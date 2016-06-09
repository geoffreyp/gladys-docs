## Install Gladys

<div class="alert alert-info" role="alert" style="padding: 10px;">Beware, this documentation is about Gladys 3.0 ! Gladys v2 is going to be deprecated soon, so don't work on it anymore :)</div>


Gladys is built on top of Node.js, and work on Linux, Mac, or Windows. This tutorial will help you install Gladys as a developer to work on a module/or on the core. 

### Prerequisites

- Node.js >= 4.2.2 ( Not compatible with Node.js v5 for the moment )
- MySQL
- Command Line Tools
 - <img src="https://developer.gladysproject.com/assets/images/documentation/apple.gif" height="17">&nbsp;**Mac OS X**: [Xcode](https://itunes.apple.com/us/app/xcode/id497799835?mt=12) (or **OS X 10.9 Mavericks**: `xcode-select --install`)
 - <img src="https://developer.gladysproject.com/assets/images/documentation/windows.jpg" height="17">&nbsp;**Windows**: [Visual Studio](http://www.visualstudio.com/downloads/download-visual-studio-vs#d-express-windows-8)
 - <img src="https://developer.gladysproject.com/assets/images/documentation/ubuntu.jpg" height="17">&nbsp;**Ubuntu**, **Debian**: `sudo apt-get install build-essential`

### Cloning Gladys

First, simply clone the repository : 

```
git clone https://github.com/GladysProject/Gladys.git gladys
```

Move into the gladys folder, and switch to the v3 branch :

```
cd gladys && git checkout v3
```


### Installing dependencies

Still in the `gladys` folder, install npm dependencies : 

```
sudo npm install && npm install -g sails && npm install -g grunt-cli
``` 

**Note :** You don't need sudo, depends of your system. Most of the time, it's not recommended.

### Environment variables

To give Gladys your MySQL credentials, you need to pass them threw environment variables. Set the followings environment variables with your own informations :

`MYSQL_HOST`, `MYSQL_PORT`, `MYSQL_USER`, `MYSQL_PASSWORD` and `MYSQL_DATABASE`.

**Dirty workaround:**

If you don't manage to set the environment variables, or want to modify permanently the config file, you can change everything in this file in Gladys => `config/connections.js`.


### Starting Gladys in development mode

Gladys is simply a Sails.js application, so in the gladys folder just type : 

```
sails lift
```

You can now access Gladys in your browser :

```
http://localhost:1337
```

### Start Gladys in production mode


First you need to compile assets ( concat + minify JS & CSS ), and init the tables in MySQL with the following command : 

```
node init.js && grunt buildProd
```

Then, to start Gladys in production, just type : 

```
node app.js
```

You can now access Gladys in your browser : 

```
http://localhost:8080
```


### Start unit tests

To start unit tests, use the grunt task :

```
grunt coverage
```

Or if you want to start tests without code coverage : 

```
grunt test
```
