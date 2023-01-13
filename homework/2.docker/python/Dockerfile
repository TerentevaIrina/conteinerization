FROM python:3.9-alpine

WORKDIR /app

ADD  requirements.txt .

RUN pip install -r /app/requirements.txt

ADD app.py .

EXPOSE 8000

ENTRYPOINT python /app/app.py 
