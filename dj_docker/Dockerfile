# imagen a ocupar, python -v 3.5
FROM python:3.5

# ENV variable de entorno

# PYTHONUNBUFFERED los errores los muestra en la consola
ENV PYTHONUNBUFFERED 1

ENV WEBAPP_DIR=/dj_docker

RUN mkdir $WEBAPP_DIR

WORKDIR $WEBAPP_DIR

ADD requirements.txt $WEBAPP_DIR/

RUN pip install -r requirements.txt

ADD . $WEBAPP_DIR/