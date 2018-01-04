PostgreSQL
===========

Sammlung von hilfreichem Wissen zur Funktionsweise von PostgreSQL, Tipps & Tricks,
Codeschnipseln, Rezepten, guten Funktionen, etc.

Zugriff auf PostgreSQL
-----------------------

ogr2ogr
~~~~~~~~

Sehr nützliches Kommandozeilenprogramm, mit dem sich schnell ein Shapefile in
PostGIS importieren lässt. Einige Dinge muss man jedoch wissen.

Verhalten von Constraints
--------------------------

:command:`PRIMARY KEY` entspricht in seinem Verhalten fast gänzlich der Kombination
aus :command:`UNIQUE` und :command:`NOT NULL`. Für manche Anwendungsfälle,
z.B. wenn Daten mit ogr2ogr importiert werden sollen, kann es nötig sein letzteres
zu verwenden. Der einzige Vorteil von PRIMARY KEY ist, dass Postgres automatisch
auf ihn zurück greift falls ein FOREIGN KEY sich auf die Tabelle bezieht ohne
eine Spalte anzugeben.