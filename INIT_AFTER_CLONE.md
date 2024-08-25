** First things first git config **
git config --global user.email "richardnv@gmail.com"
git config --global user.name "richardnv"


** set up and initialize the dev environment and admin site**
'''
cd /home/project/IBM-FS-Dev-Capstone/server

pip install virtualenv

virtualenv djangoenv

source djangoenv/bin/activate

python3 -m pip install -U -r requirements.txt

python3 manage.py makemigrations

python3 manage.py migrate

'''

** stasic pages and front end and user auth and mgmt **
'''
cd /home/project/IBM-FS-Dev-Capstone/server/frontend

npm install

npm run build

'''

** build the docker images for the mongodb and node apps **
'''
cd /home/project/IBM-FS-Dev-Capstone/server/database

docker build . -t nodeapp

docker-compose up

'''