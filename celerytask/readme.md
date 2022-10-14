To run  
cd to celerytask then

run celery with:   
celery -A celerytask worker --loglevel=info -P eventlet  

run django with:   
python manage.py runserver