#1
usar python3.6 en AWS, el 3.4 no tiene soporte para django 2.1
por lo menos es superior y deberia de correr django 2.1
#2 
no usar Docker por la configuracion Debian-flavored, EC2 es tipo Redhat

instalar el 3.5
```
apt-get install make build-essential libssl-dev zlib1g-dev libbz2-dev libsqlite3-dev
wget https://www.python.org/ftp/python/3.5.6/Python-3.5.6.tgz
sudo tar xzf Python-3.5.6.tgz
cd Python-3.5.6
sudo ./configure --enable-optimizations
sudo make altinstall
wget https://bootstrap.pypa.io/get-pip.py
sudo python3.5 get-pip.py 
```
se usa
`sudo python3.5 -m pip install bs4`

si el server de codenvy olvida el venv :
sudo python3.5 -m pip install awsebcli

python3.5 -m virtualenv venv --python=python3.5
python manage.py migrate
python manage.py createsuperuser
python manage.py runserver

