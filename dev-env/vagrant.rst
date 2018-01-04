Vagrant
========

Vagrant ist eine sehr interessante und nützliche Software, um Enwicklungsumgebungen
schnell und standardisiert einzurichten. Die Einarbeitung, das Troubleshooting
und das Verstehen der spezifischen Fallstricke benötigt jedoch einige Tage.
Insbesondere, da es nicht nur gilt Vagrant zu verstehen, sondern zusätzlich
Virtual-Box, typische Aufgaben von Sys-Admins, Linux, Apache, Shell-Skripte,
Puppet, uvm.



Vagrant einrichten
-------------------

Ein `ausführlicher Guide`_ beschreibt die Einrichtung von Vagrant mit
Port-Forwarding, Symlinks, Provisioning auf Basis von Shell-Skripten und
einigen anderen interessanten Möglichkeiten.

.. _ausführlicher Guide: http://tech.osteel.me/posts/2015/01/25/how-to-use-vagrant-for-local-web-development.html 


Installation
~~~~~~~~~~~~~

Box einrichten
~~~~~~~~~~~~~~~

Der erste Schritt ist die Auswahl einer Base-Box. Die offiziellen ubuntu-Boxen
sollen eine schlechte Qualität haben und entsprechen nicht dem Vagrant-Standard
(e.g. Nutzername und Password ist nicht "vagrant").
Hashicorp (der Hersteller von Vagrant) bietet nur eine veraltete Ubuntu 12 Base-Box an.
Hashicorp empfiehlt offiziell die Boxen im Bento-Namespace.
Mehr dazu siehe in einem `Tutorial zur Erstellung multipler Vagrant-Boxen`_.

.. _Tutorial zur Erstellung multipler Vagrant-Boxen: https://manski.net/2016/09/vagrant-multi-machine-tutorial/

Drei verschiedene Varianten für die Einrichtung einer Vagrant-Box sind denkbar:

    * VirtualBox-File wird erstellt, alles gewünschte installiert und konfiguriert
      und am Ende mit ``vagrant package`` eine Vagrant-Box daraus erstellt. Infos
      bspw. `hier`_.
    * Im *Vagrantfile* werden über den ``provisioning`` Befehl ``*.sh`` Skripte
      angegeben, in denen die Konfigurationsbefehle für Ubuntu festgehalten sind.
    * Mit dem Tool `PuPHPet`_ erstellt man sich eine Konfiguration seiner Wahl
      um bekommt die entsprechenden Skripte bereitgestellt. Als Grundlage dafür dient
      das Linux-Tool *Puppet*, welches jedoch weit mehr Einarbeitungszeit erfordern
      würde (sicherlich ein - zwei Wochen). Weitere Infos gibt es in einem `Tutorial`_.

.. _hier: https://www.vagrantup.com/docs/virtualbox/boxes.html
.. _PuPHPet: https://puphpet.com/
.. _Tutorial: https://return-true.com/beginners-guide-using-vagrant-with-puphpet-for-local-development/

Vagrant konfigurieren
----------------------

Fehler beheben
---------------

Links
------