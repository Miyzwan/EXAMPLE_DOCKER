#### Video Tutorial for this project
https://youtu.be/SQ4A7Q6_md8
<br><br>

#### Getting the files
Download zip file<br> 
or <br>
git clone command (need git to be installed) and remove git folder afterwards
```
git clone https://github.com/andyjud/django-starter.git . && rm -rf .git
```
<br><br><br>

## Setup

#### - Create Virtual Environment
###### # Mac
```
python3 -m venv venv
source venv/bin/activate
```

###### # Windows
```
python3 -m venv venv
.\venv\Scripts\activate.bat
```

<br>

#### - Install dependencies
```
pip install --upgrade pip
pip install -r requirements.txt
```

<br>

#### - Migrate to database
```
python manage.py migrate
python manage.py createsuperuser
```

<br>

#### - Run application
```
python manage.py runserver
```

<br>

#### - Generate Secret Key ( ! Important for deployment ! )
```
python manage.py shell
from django.core.management.utils import get_random_secret_key
print(get_random_secret_key())
exit()
```
### - UPDATE DARI Nizam (2702367901)

1. pada setting.py 
    delete line "ACCOUNT_EMAIL_REQUIRED = True"
    tambahkan line "ACCOUNT_SIGNUP_FIELDS = ['email*', 'username*', 'password1*', 'password2*']"

2. pada .gitignore 
    tambahkan line"staticfiles/"

3. pada setting.py 
    tambahkan linne "STATIC_ROOT = BASE_DIR / 'staticfiles'"

4. build & run docker  image
    "docker build -t django-starter ."
    "docker run -p 8000:8000 django-starter"
    kemudian acces "http://localhost:8000"




