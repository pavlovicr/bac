Navodila
======================

COOKIECUTTER
^^^^^^^^^^^^

sudo apt-get update
sudo apt-get install cookiecutter
pip install --upgrade cookiecutter
git clone git@github.com:audreyr/cookiecutter-pypackage.git

PYTHON 3.6.3
^^^^^^^^^^^^
::
iz python spletne strani download python 3.6.3, extrahiraj in pojdi v direktorij Python-3.6.3
./configure
sudo make
sudo make install

VIRTUALNO OKOLJE

sudo pip3 install virtualenv   ali pa za zadnjo verzijo
sudo pip3 install https://github.com/pypa/virtualenv/tarball/master   
virtualenv MOJEVIRTUALNO oziroma localvenv  ....kreiramo lastno virtualno okolje

UREDITEV OKOLJA za development localvenv

source localvenv/bin/activate
pip install -r requirements/local.txt  .....(mogoče sudo pip3 ?) instalira django in ostale programe

POSTGRES

sudo su -l postgres
createdb bac .........kreiramo bazo

DJANGO

python manage.py runserver
python manage.py migrate

READTHEDOCS

za lepo html obliko navodil ali tudi modelsov in ostalega
v index.rst vpišemo ime fajla "navodila"
pip install sphinx sphinx-autobuild
make html










