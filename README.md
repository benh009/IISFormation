# IIS Formation

## IIS Internet Information Services (Version 10)
IIS est Web server qui tourne sur la plateforme microsoft.net sur windows OS.

Il est possible de le faire tourner sur linux et macs avec Mono 

## IIS Express


## C'est quoi un webserver
Process message qui arrivent sur le port tcp 80(HTTP) et 443(HTTPS)
tcp couche de transport
HTTP protocol de la couche applicatif 
HTTPS version sécurisé par protocoles ssl ou tls
image (?)

## Installation (windows 10)
IIS est une fonctonnalité de windows. Il suffit de l'activer

Presser la touche Windows et Taper "Turn Windows features on or off"

![alt text](https://github.com/benh009/IISFormation/blob/master/Capture.PNG "Logo Title Text 1")


## IIS feature
### Types d'application
* Host asp.net web application 
* static website HTML5
* SFTP/FTP server 
* Host WCF service
* PHP application

Outils pour installer les modules https://www.microsoft.com/web/downloads/platform.aspx

### Authentication
* windows auth (windows active directory environment) permet d'utiliser son compte du domaine pour se connecter
* Anonyme 
* ASP.NET

### Request Filtering
* whitelisting 
* blacklisting 
* authorization  rules

## UI 
![alt text](https://github.com/benh009/IISFormation/blob/master/iis-web-server-iis-manager-18346.png "Logo Title Text 1")
3 parties
* La gauche contient les serveurs connecté. on peut utiliser le remote server 
    * applications pools
    * Sites
* Le centre contient les fonctionnalités (securité/logging)
* La droite les actions. Elle depend du context

## Application Pool

### Managed pipeline mode
integrated vs ~~ classic ~~

### worker processes
TaskManager => details w3wp.exe voir le user  
worker processes (w3wp.exe) 

ajouter une application pool crée un user. on peut le changer par des user du domaine(exemple client)

### App pool recycling 

* toute les 29h 
* change le fichier de config
![alt text](https://github.com/benh009/IISFormation/blob/master/Capture2.PNG "Logo Title Text 1")


evite d'avoir une application qui consomme toute la mémoire
## CLI 
* remote management
* using powersheel script


## static website
*Authentication 
*Default Document 
*Login
*Directory Browsing
*Mime Types

https://docs.microsoft.com/en-us/previous-versions/orphan-topics/ws.11/hh831515(v=ws.11)?redirectedfrom=MSDN

## sftp 
https://docs.microsoft.com/en-us/previous-versions/orphan-topics/ws.11/hh831655%28v%3dws.11%29

## php 

https://docs.microsoft.com/en-us/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh994589(v=ws.11)?redirectedfrom=MSDN

## .net 
https://docs.microsoft.com/en-us/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831550(v=ws.11)?redirectedfrom=MSDN
