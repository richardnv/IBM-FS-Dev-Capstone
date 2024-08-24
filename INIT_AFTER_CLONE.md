** set up and initialize the dev environment **
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

** set up and initialize the mongodb database and nodejs API **
'''
cd /home/project/IBM-FS-Dev-Capstone/server/database

docker build . -t nodeapp

docker-compose up

'''