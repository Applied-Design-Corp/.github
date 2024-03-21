## Applied Design Corperation
Welcome to Applied Design! 

Here you will find some sparse documentation regarding commonly used workflows, standards and projects.

### Using Inno Setup
Inno Setup is a program that allows us to create an installer via configuration object. This is especially useful when packaging a PyInstaller project built using onedir. 

You can download it here:
https://jrsoftware.org/isdl.php

For viable projects, there will be a folder structure that looks something like this.

```
---- Base
|
-------> Installer
    |    installer_config.iss
    | --------> Output
        |------> MyInstaller.exe

```

Double click on the .iss folder to open Inno Installer. At the top of the main file, you should see a list of defines. For example:

```
#define MyAppName "Artisan Data Analysis Tool"
#define MyAppVersion "3.2.1"
#define MyAppPublisher "Applied Design Corperation"
#define MyAppURL "https://applieddesigncorp.com/"
#define MyAppExeName "ADAT.exe"
#define ArtisanPath "C:\Users\17203\PycharmProjects\ArtisanLogViz"
```

When packaging things locally, the only thing you will need to change is the hard reference to path. Click 'compile' to rebuild the installer.exe.

