.. Informationssammlung Programmierung & Entwicklungsumgebung documentation master file, created by
   sphinx-quickstart on Thu Dec 28 14:00:25 2017.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

PHP
====

.. php:class:: DateTime

  Datetime class

  .. php:method:: setDate($year, $month, $day)

      Set the date.

      :param int $year: The year.
      :param int $month: The month.
      :param int $day: The day.
      :returns: Either false on failure, or the datetime object for method chaining.


  .. php:method:: setTime($hour, $minute[, $second])

      Set the time.

      :param int $hour: The hour
      :param int $minute: The minute
      :param int $second: The second
      :returns: Either false on failure, or the datetime object for method chaining.

  .. php:const:: ATOM

      Y-m-d\TH:i:sP
   
   
Übersichtsseite!
=================

`So schreibt man einen Link`_.

.. _So schreibt man einen Link: http://rtd-dev-stuff.readthedocs.io/en/latest/

* eine
* Liste
    * eine
    * Sub-Liste
* nun
* Ende

#. automatisch
#. nummerierte
#. Liste

*kursiv*
**fett**
``Abschnitt mit Code, [Return]
der zweizeilig ist.``

``Abschnitt mit Code, \n
der zweizeilig ist.``

``Abschnitt mit Code,``
``der zweizeilig ist.``

Und hier ein Codeblock::

    Abschnitt mit unformatiertem Code,
    der zweizeilig ist.

| Diese Zeilen
| werden genau wie gewollt
| umgebrochen.

`Inline Link <http://example.com/>`_
    
Führe diese ``Anweisungen`` aus, der Doppelpunkt am Ende der Zeile ist dabei
wichtig um das Folgende verkleinert und in einer Code-Box darzustellen::

    $ vagrant up

Then in your ``conf.py``:

.. code-block:: python

    from things import a-thing
    while 1 == True:
        print("An endless loop")

.. note:: Wichtige Infos
          die in einem blauen Infokasten
          hervorgehoben werden sollen.
    
Hier ist ein Link innerhalb derselben Seite (desselben ``*.rst`` Dokuments): :ref:`springe-zu-anker`.

Und so springt man zu einem anderen Dokument (anderer ``*.rst`` Datei) :doc:`dev_env`.

.. _springe-zu-anker:

.. toctree::
   :maxdepth: 2
   :caption: Hier ist der Anker zu dem gesprungen wurde!

   name-der-einzubindenden-rst
   dev_env