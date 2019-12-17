# IIS Formation

## IIS Internet Information Services (Version 10)
IIS est Web serveur qui tourne sur la plateforme microsoft.net sur windows OS.

Il est possible de le faire tourner sur Linux et Macs avec Mono 

IIS Express est la version légère souvent utilisé avec Visual Studio


## Webserver ?
Process les requêtes qui arrivent sur le port tcp 80(HTTP) et 443(HTTPS)
* TCP couche de transport
* HTTP protocol de la couche applicatif 
* HTTPS version sécurisé par protocoles ssl ou tls

## Installation (Windows 10)
IIS est une fonctonnalité de Windows. Il suffit de l'activer

Presser la touche Windows et Taper "Turn Windows features on or off"

![alt text](https://github.com/benh009/IISFormation/blob/master/Capture.PNG "Logo Title Text 1")

## IIS feature
### Types d'application
* Static Website HTML5
* Host asp.net Web application 
* PHP application
* SFTP/FTP server 
* Host WCF service


Outils pour installer les modules https://www.microsoft.com/web/downloads/platform.aspx

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
* La gauche contient les serveurs connecté. on peut utiliser le remote server 
    * Applications pools
    * Sites
* Le centre contient les fonctionnalités (securité/logging,...)
* La droite les actions. Elle dépend du context

## Application Pool

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
## CLI 
* Remote management
* Using powersheel script


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


## FTP SFTP 
[Plus](https://docs.microsoft.com/en-us/previous-versions/orphan-topics/ws.11/hh831655%28v%3dws.11%29
user iss management)

## .NET 
[Plus](https://docs.microsoft.com/en-us/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831550(v=ws.11)?redirectedfrom=MSDN)
