Python Tricks
==================

Commandline commands
---------------------

.. code:: python

    py -3
    python --version
    pip --version
    pip install --user pipenv
    python -m pip install <package-name>
    pip freeze > requirements.txt
    pip install -r requirements.txt
    
Background
~~~~~~~~~~~
**pipenv** ist ein dependency manager für Python und mächtiger als pip alleine. 
Er erstellt automatisch virtuelle Umgebungen. Mit der ``--user`` Option soll 
verhindert werden, dass systemweite Packages beschädigt werden. Sollte 
nach der Installation *pipenv* nicht per *cmd* aufrufbar sein, muss der Pfad 
``C:\Users\Flo\AppData\Roaming\Python\Python36\Scripts`` manuell in die 
PATH-Variable von Windows eingefügt werden.