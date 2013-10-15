Homepage
========

A very basic homepage to replace my iGoogle page. 

Currently, no backend is necessary, but this may change if some feature needs one.

Warning
-------

This is a personal project, and features are only added as I need them. The code is up for people who might be interested, but in no way should this be considered *good code*. Things are mostly hacked together so that they will work **for me**.

Developper installation
-----------------------

The following tools are needed:

 - NodeJS and npm
 - Yeoman `npm install -g yo`
 - *(Optional)* generator-angular `npm install -g generator-angular`

Clone the repo, and then run `npm install && bower install` to download the dependencies.

Deployment
----------

Run `grunt build` to build the project. This will create a dist folder with everything needed to run the app. Note that the way things are setup right now, the `bower_components` folder does not have to be deployed.

You can setup FTP publishing by editing `Gruntfile.js`. Find the line containing `ftp-deploy` and edit to your liking. Then, add an `.ftppass` file to the root of the project, containing this:

```json
{
    "your.ftp-server.address.com": {
        "username": "your_username",
        "password": "your_password"
    }
}
```

This file is gitignored.

You should then be able to run `grunt build ftp-deploy` to build the project and push the dist folder to your FTP server.