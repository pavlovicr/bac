Osnovni ukazi
=============

Linux
^^^^^^^^^^^^^^^^^^^^^

Ustvarjanje fajlov in vsebin
----------------------------

ustvari nov fajl
::
	touch vaja1.txt
insert tekst "miha kovacev" v vaja1.txt in zbriši predhodni tekst
::
	echo “miha kovacev” > vaja1.txt
insert nov tekst k predhodnemu
::
	echo "županova micka2 >> vaja1.txt
poglej vsebino fajla vaja1.txt
::
	cat vaja1.txt
ustvari nov fajl in kopiraj vsebino iz fajla vaja1.txt
::
	cat ”vaja1.txt” > vaja2.txt 






PYTHON
^^^^^^
instalacija Pythona
-------------------

download iz https://www.python.org/downloads/python3.6.3
iz download direktorija Python-3.6.3 izvršimo ukaze
::
    ./configure
    sudo make
    sudo make install

delo z moduli
-------------

informacije o modulu datetime dirktno iz linux terminala
::
	pydoc datetime

kodo, ki je vpisana pod tem izrazom zažene samo takrat, ko poženemo izvirni fajl
in ne z >>> import mojmodul.
Koristno pri delu s testi, ki so sestavni del kode na istem fajlu
::
	if __name__ == '__main__':

instalacija lastnih modulov v site-packages, ki se nahaja v 
home/pavlovicr/virtualno_test/lib/python3.5/site-packages
::
	>>>import sys
	>>>sys.path.append('~/vaja')
	>>>import vaja 
	>>>import primer

izpis imena modula , ki je bil importan 
primer za ime modula 'time'
::
	>>> import time
	>>> time.__name__	 
delo s časom 
::
	>>> import datetime
primer tekoče ure
	>>>a=datetime.datetime.now().hour
lahko tudi
	>>>import datetime
	>>>from datetime import datetime
	>>>a=datetime.now()
	>>>a.hour
	>>>a.minute
	>>>a.day
primer 12 sekund do izklopa
::
	>>>import time	
	>>>time.sleep(12)
primer današnji dan
::
	>>>time.localtime().tm_mday
primer danes
::
	>>>time.asctime()

razno
-----
seznam instaliranih programov
::
	pip freeze

testiranje
izpis izvajanja testa kode, ko je test sestavni del kode
::
	python vaja.py -v


VIRTUALNO OKOLJE
----------------
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

mogoče je treba s sudo pip3
v requirements/local.txt so naloženi programi za development
::
	source LOCAL/bin/activate
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

	django-admin startproject . # s piko ne ustvari nepomembnega direktorija


COOKIECUTTER
^^^^^^^^^^^^
::
 
    sudo apt-get update
    sudo apt-get install cookiecutter
    pip install --upgrade cookiecutter
    git clone git@github.com:audreyr/cookiecutter-pypackage.git





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







