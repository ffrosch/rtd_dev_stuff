Auerhuhn-DB
============

Shapefile laden
----------------
.. note:: ACHTUNG: ogr2ogr kann keine Daten in ein PRIMARY KEY-Feld einfügen.
          Es akzeptiert nur PRIMARY KEY Felder die als SERIAL deklariert sind.
          Was hingegen funktioniert ist CONSTRAINT UNIQUE zusammen mit NOT NULL.

Vorgehen:
    #. Im Verzeichnis mit dem gewünschten Shapefile: :guilabel:`Shift + Rechtsklick`
    #. Auswählen: :command:`Eingabeaufforderung hier öffnen`
    #. Eintippen: "ogr2ogr ...", Enter
