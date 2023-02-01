FROM python:3.11-slim-buster
ENV PYTHONBUFFERED=1

WORKDIR /app

COPY requirements.txt /app/requirements.txt

RUN pip3 install -r requirements.txt

COPY . /app
EXPOSE 8000

#for development
CMD ["manage.py","runserver"]

#for production
#CMD ["gunicorn","--bind","0.0.0.0:8000","superadmin.wsgi:application"]