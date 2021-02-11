FROM python:alpine
WORKDIR /app
COPY . .
RUN python -m venv venv
RUN source ./venv/bin/activate
RUN python -m pip install -r requirements.txt
RUN python manage.py makemigrations
RUN python manage.py migrate
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
