Apache
=======

**Apache** ist neben **nginx** (sprich: *engine-x*) der klassische Provider für
Http-Services.

Hilfreiche Informationen finden sich bspw. auf der `Ubuntu-Website`_.

.. _Ubuntu-Website: https://wiki.ubuntuusers.de/Apache_2.4/

Server einrichten
------------------

Installation über Ubuntu-Terminal::

    sudo apt-get install apache2

.. note:: Der Apache-Server wird nach der Installation sofort gestartet und
          wird bei jedem Neustart automatisch geladen. Er läuft auf 
          **localhost** Port **80**.

.. note:: Bei der Verwendung von **Vagrant** muss im *Vagrantfile* ein
          Port-Forwarding eingerichtet werden.

Port-Forwarding in Vagrant::

    config.vm.network :forwarded_port, guest: 80, host: 8080

Websites in der Virtuellen Maschine sind nun über **localhost:8080** im
Browser aufrufbar.

Server konfigurieren
---------------------