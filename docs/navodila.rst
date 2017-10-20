Za uvod linux komande
^^^^^^^^^^^^^^^^^^^^^
::

	touch mojfile
	echo “ratata” > mojfile
	cat ”mojile” > mojfile1 …...vsebina iz moj file se skopira v mojfile1
	cat mojfile ….ogled vsebine

	django-admin startproject .  …..s piko ne ustvari nepomembnega direktorija



Django instalacija koplet
=========================



COOKIECUTTER
^^^^^^^^^^^^
::
 
    sudo apt-get update
    sudo apt-get install cookiecutter
    pip install --upgrade cookiecutter
    git clone git@github.com:audreyr/cookiecutter-pypackage.git

PYTHON 3.6.3
^^^^^^^^^^^^

pojdi na https://www.python.org/downloads/python3.6.3
extrahiraj in pojdi v direktorij Python-3.6.3
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
    virtualenv LOCAL(MOJE VIRTUALNO OKOLJE) 

OKOLJE ZA DEVELOPMENT(LOCAL)
^^^^^^^^^^^^^^^^^^^^^
::
mogoče je treba s sudo pip3
v requirements/local.txt so naloženi programi za development
	source LOCAL/bin/activate
	pip install -r requirements/local.txt

POSTGRES_::
^^^^^^^^

v serverju postgres ustvarimo bazo
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

text = """
.. _top:

Hello world
===========
Hello world
^^^^^^^^^^^
Hello word
----------



(1) zamiki

* zamik "*"
  
  - zamik še enkrat "-"

    + in še enkrat







