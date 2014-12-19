TestingCentre
=============

A project for learning how ZF2 works, following along with the code from *Learn ZF2: Learning By Example*.

### Adding New Submodules

This method of adding ZF2 skeleton modules as git submodules creates a clone of the ZF2 skeleton module in your own personally hosted repo, so that you can make changes to the ZF2 skeleton application. 

1. Create a new repo on your Github account for the module, e.g. ```MyModule```
2. On your local machine, outside of your ZF2 application, clone the ZF2 skeleton module to any location. This will be temporary ```~/Documents $ git clone https://github.com/zendframework/ZendSkeletonModule.git MyModule```
3. cd into the newly cloned module, and change the remote repo that the local one points to: ```~/Documents/MyModule $ git remote set-url origin https://github.com/mygithubusername/MyModule.git```
4. Push up the changes: ```~/Documents/MyModule $ git push```
5. Go into your ZF2 application and into the modules/ directory. Once there, add your new MyModule repo as a submodule: ```~/Path/To/ZF2Application/modules $ git submodule add https://github.com/mygithubusername/MyModule.git```
6. You can now delete the temporary folder knowing your module is safe on Github and will be referenced as a submodule by your application, and any others you wish to include. 
7. Look into composer...


### PHP CLI Server

The simplest way to get started if you are using PHP 5.4 or above is to start the internal PHP cli-server in the root directory:

    php -S 0.0.0.0:8080 -t public/ public/index.php

This will start the cli-server on port 8080, and bind it to all network
interfaces.

**Note: ** The built-in CLI server is *for development only*.


