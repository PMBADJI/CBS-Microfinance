web: sh -c 'python manage.py migrate && gunicorn config.wsgi:application --bind 0.0.0.0:${PORT:-8000} --workers 4 --timeout 120'
worker: celery -A config worker --loglevel=info
beat: celery -A config beat --loglevel=info
