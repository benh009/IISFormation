# IIS Formation

## Agenda 
* [IIS Internet Information Services (Version 10)](https://github.com/benh009/IISFormation/blob/master/README.md#iis-internet-information-services-version-10)
* [Webserver ?](https://github.com/benh009/IISFormation/blob/master/README.md#webserver-)
* [Rappels sur les notions réseaux](https://github.com/benh009/IISFormation/blob/master/README.md#rappels-sur-les-notions-r%C3%A9seaux)
* [Installation (Windows 10)](https://github.com/benh009/IISFormation/blob/master/README.md#installation-windows-10)
* [IIS fonctionnalités](https://github.com/benh009/IISFormation/blob/master/README.md#iis-fonctionnalit%C3%A9s)
* [UI ](https://github.com/benh009/IISFormation/blob/master/README.md#ui)
* [Command-line interface (CLI)](https://github.com/benh009/IISFormation/blob/master/README.md#command-line-interface-cli)
* [Static Website](https://github.com/benh009/IISFormation/blob/master/README.md#static-website)
* [PHP](https://github.com/benh009/IISFormation/blob/master/README.md#php)
* [ Application Pool](https://github.com/benh009/IISFormation/blob/master/README.md#application-pool)
* [FTP SFTP ](https://github.com/benh009/IISFormation/blob/master/README.md#ftp-sftp)
* [.NET ](https://github.com/benh009/IISFormation/blob/master/README.md#net)
* [Démonstration ](https://github.com/benh009/IISFormation/blob/master/README.md#d%C3%A9monstration)
* [Exercices](https://github.com/benh009/IISFormation/blob/master/README.md#exercices)

## IIS Internet Information Services (Version 10)
IIS est un Web serveur qui tourne sur la plateforme microsoft.net sur Windows OS.

Il est possible de le faire tourner sur Linux et Macs avec Mono. 

IIS Express est la version légère souvent utilisée avec Visual Studio.


## Web server ?
Il héberge des ressources (pages web, images, vidéos, etc.) du Web.

Ces ressources peuvent être statiques (servies telles-quelles) ou dynamiques (construites à la demande par le serveur). 

Pages web qui sont généralement rendues en HTML

Exemples de Web servers
* Apache HTTP Server 
* Apache Tomcat
* nginx 
* NodeJS 

## Rappels sur les notions réseaux

Process les requêtes qui arrivent sur le port tcp 80(HTTP) et 443(HTTPS)
* TCP couche de transport
* HTTP protocol de la couche applicatif 
* HTTPS version sécurisé par protocoles ssl ou tls
![alt text](https://github.com/benh009/IISFormation/blob/master/Capture4.PNG  "Logo Title Text 1")
DNS : 

![alt text](https://github.com/benh009/IISFormation/blob/master/Capture3.PNG  "Logo Title Text 1")
* Stateless Model vs Stateful Model
   * Cookie
## Installation (Windows 10)
IIS est une fonctonnalité de Windows. Il suffit de l'activer.

Presser la touche Windows et Taper "Turn Windows features on or off".

![alt text](https://github.com/benh009/IISFormation/blob/master/Capture.PNG "Logo Title Text 1")

## IIS fonctionnalités
### Types d'application
* Static Website HTML5
* Host asp.net Web application 
* PHP application
* SFTP/FTP server 
* Host WCF service


Outils pour installer les modules [Web Platform Installer](https://www.microsoft.com/web/downloads/platform.aspx)

### Authentication
* Windows authentification (Windows active directory environment) permet d'utiliser son compte du domaine pour se connecter
* Anonyme 
* ASP.NET

### Request Filtering
* Whitelisting 
* Blacklisting 
* Authorization rules

## UI 
![alt text](https://github.com/benh009/IISFormation/blob/master/iis-web-server-iis-manager-18346.png "Logo Title Text 1")
Trois parties
* La gauche contient les serveurs connectés. on peut utiliser le remote server 
    * Applications pools
    * Sites
* Le centre contient les fonctionnalités (securité/logging,...)
* La droite les actions. Elle dépend du context

## Command-line interface (CLI)
* Remote management
* Using powersheel script

run cmd as admin
```
cd C:\Windows\System32\inetsrv
```


```

appcmd add site /name:"Dummy Site" /id:10 /bindings:http/*:81:
appcmd add app /site.name:"Dummy Site" /path:"/"

appcmd add vdir /app.name:"Dummy Site/" path:"/"

appcmd set vdir "Dummy Site/" /physicalPath:"c:\inetpub\wwwroot"
```


Egale à 

```

appcmd add site /name:"Dummy Site" /id:10 /bindings:http/*:81: /physicalPath:"c:\inetpub\wwwroot"
```

Liste les sites 

```

appcmd list app
```


Listes les backups de configuration 

```

appcmd list app
```


```

iisreset /stop
```


## Static Website
* Authentication 
* Default Document 
* Logging
* Directory Browsing
* Mime Types

On peut ajouter du Javascript car le code est exécuté coté client. 

[Plus]( https://docs.microsoft.com/en-us/previous-versions/orphan-topics/ws.11/hh831515(v=ws.11)?redirectedfrom=MSDN)

## PHP

[Plus](https://docs.microsoft.com/en-us/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh994589(v=ws.11)?redirectedfrom=MSDN)


## Application Pool
Application Pool = sécurité (isolation user)
### Managed pipeline mode
integrated vs ~~classic~~

### worker processes
TaskManager => details w3wp.exe voir le user  
Worker processes (w3wp.exe) 

Ajouter une application pool crée un user. On peut le changer par des user du domaine(exemple client)

### App pool recycling 

* Toute les 29h 
* Change le fichier de config
![alt text](https://github.com/benh009/IISFormation/blob/master/Capture2.PNG "Logo Title Text 1")


Evite d'avoir une application qui consomme toute la mémoire

## FTP SFTP 
[Plus](https://docs.microsoft.com/en-us/previous-versions/orphan-topics/ws.11/hh831655%28v%3dws.11%29)

User iss management

Client Ftp : [FileSilla](https://filezilla-project.org/)
## .NET 
[Plus](https://docs.microsoft.com/en-us/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831550(v=ws.11)?redirectedfrom=MSDN)


## Exercices 

### Site static + php
* Logger les connections dans un fichier séparé tout les heures 
   * Date et Adresse ip
   
### .NET 
* Deployer un website

### FTP 
* User Admin
* Créer un dossier privé à USER2 et USER2 
* Créer un dossier partagé entre USER1 et USER2 en lecture
* User Admin est le seul à acceder modifier le dossier partagé
* Accepter unique des fichiers .txt et .png

## Démonstration 
 [Web Platform Installer](https://www.microsoft.com/web/downloads/platform.aspx)
* Wordpress
