# Needs Map 

Needs Map
A  project aimed at locating the missing gaps after freedome Sryia become real in in 8.12.2021

The project emerged after Syria become free, which there is alot of needes to be located . We launched a technology platform to coordinate devlopment efforts.

https://Smart-Syria.com/




## Project features

 - Pin on the map to notice a a need:
Where the contrbuter of the need can put a pin on the map for the place with there with name, description, and phone number.

 - Search on map 
NGOs can browse the map and search for the related quilfecations in the area where they are working.

 - Add a go-to location button, a link showing the location on google maps 
 
 - Allow adding multiple needes in one pin (need for Schools Hospital .... )
 
 - Automatically update an excel sheet on every new change in dB
 
 - Add new pins type (scholl, in hospital, need help, found), thess pins shows with 4 differnt collers on map
 
 - Updating state is ready as backend through Gmail authentication, the person who made the report can update the status (only backend needs a frontend)
 
 - Add search-by-name bar
 
 - frontend for the update status (table page needs to login)

## Missing:
 - Enhance UI/UX 
 - add image/s to missing pin (Need legal approval)
 
### NOTE : You can create pull request to ``new_development`` branch for development.
 
## HOW TO RUN THE PROJECT (without docker)
1. clone the project
```
git clone https://github.com/tarifkhashaneh/needs-gaps.git
```
2. change the branch for ``new_development`` branch with this command :
```
git checkout new_development
```

3. create python virtual environment and activate it from terminal (ubuntu & mac) 
```
cd DepremKayiplari
virtualenv env
```
then activate the env
```
source env/bin/activate
```
4. create .env file (ubuntu & mac) 
```
touch .env
```
5. fill the .env params
```
DEBUG=True
SECRET_KEY=< Your SECRET_KEY>
```
- **you can use sqlite for development pourpes**
 go to `appname/setting.py` Line 94 and comment out
 ```
  DATABASES = {
     'default': {
         'ENGINE': 'django.db.backends.sqlite3',
         'NAME': BASE_DIR / 'db.sqlite3',
     }
 }
```
 and comment from line 101 to 110
 
6. install dependecies 
```
pip3 install -r requirements.txt
```
7. migrate the DB
```
python manage.py makemigrations
```
```
python manage.py migrate
```
8. run the app 
```
python manage.py runserver
```

 
