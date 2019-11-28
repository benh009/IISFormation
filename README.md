# IIS Formation

## IIS Internet Information Services(version 10)
web server qui tourne sur la plateforme microsoft.net sur windows os
Il est possible de le faire tourner sur linux et macs avec Mono 

## IIS Express


## C'est quoi un webserver
Process message qui arrivent sur le port tcp 80(HTTP) et 443(HTTPS)
tcp couche de transport
HTTP protocol de la couche applicatif 
HTTPS version sécurisé par protocoles ssl ou tls
image (?)

## Installation (windows 10)
IIS est une fonctonnalité de windows . Il suffit de l'activer
Presser la touche Windows et Taper "Turn Windows features on or off"
Inline-style: 
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


## CLI 
* remote management
* using powersheel script
