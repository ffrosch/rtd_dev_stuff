DB-Frontend
============

Bisher gibt es im Arbeitsbereich Wildtierökologie kein schlüssiges und einheitliches
Konzept zur langfristigen Speicherung von Daten.

Anforderungen
--------------

Schlüsselanforderungen:

    * Datenkonsistenz
    * Einfachheit der Eingabe, Abfrage und Korrektur
    * Daten liegen an einem zentralen Ort und sind auch in 10 Jahren noch auffindbar und nachvollziehbar

Erweiterte Anforderungen:

    * User-Login auf Basis von Windows SSO (LDAP/Kerberos)
    * Erstellung von benutzerdefinierten Views im DB-Schema des Benutzers
    
Software
---------

    * Apache
    * PHP (Codeigniter-Framework)
    * Bootstrap
    * JavaScript Bibliotheken für interaktive Tabellen
    * PostGIS
    * 