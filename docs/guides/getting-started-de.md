# Erste Schritte mit der Companyname Cloud API

Um die Companyname Cloud zu nutzen, können Sie entweder den webbasierten [Data Center Designer (DCD)](https://dcd.companyname.com/ "Companyname Data Center Designer öffnen") oder die Companyname Cloud API verwenden. Eine API (Application Programming Interface) ist eine programmatische Schnittstelle, über die Sie mit Diensten interagieren können, um Ressourcen zu verwalten und zu steuern. In diesem Artikel wird anhand eines einfachen Beispiels erklärt, wie Sie eine API-Anfrage ausführen.

## Verwendung von API-Anfragen
1. [Authentifizieren Sie sich](https://docs.companyname.com/cloud/reference/get-started?q=authent#authorization "Lesen Sie, wie Sie sich authentifizieren") an der Companyname API.
2. Verwenden Sie einen HTTP-GET-Befehl, um eine Liste aller Benutzer abzurufen, die im Verzeichnis /v1/users gespeichert sind: `curl GET https://example.com/v1/users`
	
	
	
	
Editors note:
* I did not translate the API commands/requests because usually there is no translation for API commands/arguments 