To run  
cd to celerytask then

run celery with:  
celery -A celerytask worker --loglevel=info -P eventlet  

run django with:   
python manage.py runserver  

Database details

  
        'ENGINE': 'django.db.backends.postgresql',  
        'NAME': 'celery_task_final',
        'USER': 'postgres',
        'PASSWORD': '1234',
        'HOST': 'localhost',
        'PORT': '5432',    

celery details  
CELERY_BROKER_URL = 'redis://localhost:6379'  

CELERY_ACCEPT_CONTENT = ['application/json']  

CELERY_RESULT_SERIALIZER = 'json'  

CELERY_TASK_SERIALIZER = 'json'  

CELERY_TIMEZONE = 'Asia/Kolkata'  

CELERY_RESULT_BACKEND = 'django-db'  

CELERY_CACHE_BACKEND = 'django-cache'  

CELERY_RESULT_EXTENDED = True