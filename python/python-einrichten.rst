Python einrichten
==================

`Übersicht`_. 

.. _Übersicht: http://docs.python-guide.org/en/latest/dev/env/

Python für Windows nutzen
--------------------------

Python-Package mit pip aus der Kommandozeile installieren. Hierbei steht
``-m`` für "Modul". Python weiß also, dass es das Kommando and das Modul
"pip" weitergeben soll.

.. code:: python

    python -m pip install <package-name>
    
    
Python in Atom (IDE)
~~~~~~~~~~~~~~~~~~~~~

#. Install Atom
#. Go to Atom -> Settings -> Install, search for *atom-ide-ui* and install
#. ``pip install python-language-server``
#. Go to Atom -> Settings -> Install, search for *script* and install (afterwards python files can be run with :guilabel:`Ctrl + Shift + b`)
#. Go to Atom -> Settings -> Install, search for *autocomplete-python* and install, choose engine *Jedi*
#. :guilabel:`Ctrl + Shift + p` -> Listed alle verfügbaren Kommandos auf
#. :guilabel:`Ctrl + Shift + Alt + o` -> Script: Run Options, ermöglicht z.B. das Starten der virtuellen Python-Umgebung
#. :guilabel:`Ctrl + Shift + Alt + b` -> Script: Run With Profile, ermöglicht das nutzen zuvor gespeicherter Profile

Launch Atom: das beste ist, Atom im Verzeichnis mit dem eigenen Projekt zu öffnen.
So bekommmt man vollen Zugang zu den Environment-Variablen.
``Shift + Rechtsklick -> cmd -> "atom ."``


Virtualenvironments in Python
------------------------------

Pipenv
~~~~~~~
Pipenv managed Pakete auf Projekt-Basis. Außerdem führt es eine Liste über alle
zur Zeit installierten Pakete in einem Projekt, die genutzt werden kann,
um dieses Projekt zu replizieren.

#. Check ob neueste Python Version installiert ist ``python --version``
#. Check ob *pip* installiet ist ``pip --version``
#. Installiere Paket- und Umgebungsmanager ``pip install --user pipenv``
#. Check ob ``pipenv --version`` funktioniert, falls nicht füge ``C:\Users\Flo\AppData\Roaming\Python\Python36\Scripts`` zur PATH Variablen hinzu
#. ``cd path\to\myproject``
#. ``pipenv install [package]``

Venv
~~~~~
Integrated into Python 3.6.

#. ``python3 -m venv /path/to/new/virtual/environment``
#. :guilabel:`Shift + Rechtsklick` in Projektordner -> cmd -> ``..\Scripts\activate`` aktiviert die virtuelle Umgebung. ``Pip install`` etc. funktionieren
#. ``deactivate`` deaktiviert sie