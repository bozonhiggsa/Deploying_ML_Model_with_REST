FROM python:3.8

WORKDIR /server

COPY requirements.txt ./
RUN pip install --no-cache-dir -r requirements.txt

RUN export PYTHONPATH='${PYTHONPATH}:/server'

COPY . .

# EXPOSE don't work on heroku
#EXPOSE $PORT

# We will get PORT randomly from heroku
CMD gunicorn server:app -w 4 --bind=0.0.0.0:$PORT -k uvicorn.workers.UvicornWorker
