release: python manage.py migrate --no-input
web: gunicorn --bind :$PORT --workers 4 --worker-class uvicorn.workers.UvicornWorker saleor.asgi:application
celeryworker: celery -A worker saleor.celeryconf:app --loglevel=info -E
