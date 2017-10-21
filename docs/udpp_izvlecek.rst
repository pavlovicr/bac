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



Django instalacija koplet
=========================



COOKIECUTTER
^^^^^^^^^^^^
::
 
    sudo apt-get update
    sudo apt-get install cookiecutter
    pip install --upgrade cookiecutter
    git clone git@github.com:audreyr/cookiecutter-pypackage.git



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

informacije o modulu datetime
::
	pydoc datetime

instalacija lastnih modulov v site-packages, ki se nahaja v 
home/pavlovicr/virtualno_test/lib/python3.5/site-packages
::
	>>>import sys
	>>>sys.path.append('~/vaja')
	>>>import vaja 
	>>>import primer

seznam instaliranih programov
::
	pip freeze

python primer.py -v ....se izpie izvajanje testa, ko je dodano testiranje kode


DELO Z DATUMI

import datetime
>>>a=datetime.datetime.now().hour  ......da tekoco uro
lahko tudi
>>>import datetime
>>>from datetime import datetime
>>>a=datetime.now()
>>>a.hour
>>>a.minute
>>>a.day

>>>import time
>>>time.sleep(12) ....12 sekund do izklopa
>>>time.localtime().tm_mday.........da dananji dan
>>>time.asctime() .....danes

>>>time.__name__ .....izpie ime modula v kolikor je bil naloen z import
if __name__ == '__main__': .....zazene kodo pod __name__ == '__main__' samo ce zazenemo izvirni fajl in ne z import file




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







