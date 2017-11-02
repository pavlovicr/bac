Django instalacija koplet
=========================



COOKIECUTTER
^^^^^^^^^^^^
::
 
    sudo apt-get update
    sudo apt-get install cookiecutter
    pip install --upgrade cookiecutter
    git clone git@github.com:audreyr/cookiecutter-pypackage.git
	cookiecutter cookiecutter-pypackage 

lahko pa kar direktno 
::

	cookiecutter git@github.com:audreyr/cookiecutter-pypackage.git


PYTHON 3.6.3
^^^^^^^^^^^^
v Ubuntuju je že instaliran. Ne ravno zadnja različic.
sicer pa pojdi na https://www.python.org/downloads/python3.6.3
extrahiraj in v direktoriju Python-3.6.3
::

    ./configure
    sudo make
    sudo make install

VIRTUALNO OKOLJE
^^^^^^^^^^^^^^^^

sudo pip3 install https://github.com/pypa/virtualenv/tarball/master je opcija z zadnjo verzijo
LOCAL je ime novega virtualnega okolja, ki ga bomo rabili za development
::

    sudo pip3 install virtualenv 
    sudo pip3 install https://github.com/pypa/virtualenv/tarball/master    
    virtualenv local(moje virtualno okolje) 

OKOLJE ZA DEVELOPMENT(local)
^^^^^^^^^^^^^^^^^^^^^

mogoče je treba s sudo pip3
v requirements/local.txt so naloženi programi za development
???? preberi si kako spremenimo requirements itd 

::
	source local/bin/activate
	pip install -r requirements/local.txt

POSTGRES
^^^^^^^^

v serverju postgres ustvarimo bazo
::
	sudo su -l postgres
	createdb bac 

DJANGO
^^^^^^
::

    python manage.py runserver
    python manage.py migrate

READTHEDOCS
^^^^^^^^^^^
::
za lepo html obliko navodil ali tudi modelsov in ostalega
v index.rst vpišemo ime fajla "navodila"
	pip install sphinx sphinx-autobuild
	make html


