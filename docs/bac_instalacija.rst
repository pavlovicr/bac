Django instalacija koplet
=========================

COOKIECUTTER S PREDNASTAVLJENIM DJANGOM
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
mogoče, boš moral zagnati v virtualnemu okolju.
Mislim, da zaradi poti do pythona
::
 
    sudo apt-get update
    sudo apt-get install cookiecutter
    pip install --upgrade cookiecutter
    cookiecutter https://github.com/pydanny/cookiecutter-django 

Lahko pa cloniraš projekt iz githuba in nadaljuješ naprej po istem postopku.
::

	git clone https://github.com/pavlovicr/bac  

VIRTUALNO OKOLJE in OKOLJE ZA DEVELOPMENT
^^^^^^^^^^^^^^^^
V virtualnemu okolju, ki smo ga poimenovali local in v direktoriju bac inštaliramo okolje za development z vsemi potrebnimi programi. tudi za postgres.
::

	source local/bin/activate
	cd bac
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


