** First things first git config **
git config --global user.email "richardnv@gmail.com"
git config --global user.name "richardnv"


** set up, initialize, and activate the django virtual environment **
cd /home/project/IBM-FS-Dev-Capstone/server
pip install virtualenv
virtualenv djangoenv
source djangoenv/bin/activate

** install python requirements, make all migrations, migrate, and start the admin server **
python3 -m pip install -U -r requirements.txt
python3 manage.py makemigrations
python3 manage.py migrate
python3 manage.py runserver


** install requirements for node stasic, front end, user auth, and admin pages **
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