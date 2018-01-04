Entwicklungsumgebung unter Windows
===================================

Eine Entwicklungsumgebung lässt sich unter Windows am schnellsten einrichten,
wenn man Vagrant, etc. umgeht. Für mich hat sich der Einsatz von `Uniform-Webserver`_
oder `XAMPP`_ zusammen mit PostgreSQL bewährt.

    #. **PostgreSQL** - ist eine Installation möglich, sollte diese Variante gewählt werden.
       PostgreSQL wird dann automatisch in den Autostart von Windows eingetragen,
       sodass der Server stets läuft und verfügbar ist. Alternativ bietet sich aber
       auch die Einrichtung als portable Version an. Siehe dazu dieses `Tutorial`_.
    #. **Apache-Webserver** - dieser wird für die Entwicklung mit PHP benötigt. 
       Eine XAMPP-Installation ist hierfür gut geeignet. Für die Nutzung mit PostgreSQL
       müssen unter ``c:\xampp\php\php.ini`` die beiden Zeilen ``extension=php_pdo_pgsql.dll``
       und ``extension=php_pgsql.dll`` auskommentiert werden. In der ``C:\xampp\apache\conf\httpd.conf``
       wird noch der Befehl ``LoadFile "C:\xampp\php\libpq.dll"`` eingetragen.
       Zuletzt muss sichergestellt werden, dass die Ports 80 und 443 nicht von anderen Programmen
       belegt sind. Eine Änderung der Ports für Apache ist in Xampp zwar möglich,
       scheint aber nicht out-of-the-box zu funktionieren. Die Ports werden i.d.R. durch Skype
       oder durch die Windows-Informationsdienste belegt. Für Skype lässt sich dies
       unter den Erweiterten Optionen ändern. Die Windows-Informationsdienste können
       über Systemsteuerung > Programme > Windows-Funktionen aktivieren oder deaktivieren
       ausgeschaltet werden (Menüpunkt "Internetinformationsdienste").

Nun ein schneller Test, um zu sehen ob Postgres über den Apache-Server ansprechbar ist.
Hierfür wird eine PHP-Datei unter ``c:\xampp\htdocs`` mit folgendem Inhalt erstellt:

.. code-block:: php

    <?php
    $link = pg_connect("host=localhost port=5432 dbname=postgres user=postgres password=mypassword");
    print_r($link);
    ?>

Funktioniert die Abfrage wird ein Wert ausgegeben, andernfalls ein Error!
   
.. _Uniform-Webserver: http://www.uniformserver.com/
.. _XAMPP: https://www.apachefriends.org/de/index.html
.. _Tutorial: http://www.postgresonline.com/journal/archives/172-Starting-PostgreSQL-in-windows-without-install.html