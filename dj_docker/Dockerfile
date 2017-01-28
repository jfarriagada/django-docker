# imagen a ocupar, python -v 3.5
FROM python:3.5

# esperar variable de entorno
ARG DJANGO_ENV

# ENV variable de entorno

# PYTHONUNBUFFERED los errores los muestra en la consola
ENV PYTHONUNBUFFERED 1

ENV WEBAPP_DIR=/dj_docker

RUN mkdir $WEBAPP_DIR

WORKDIR $WEBAPP_DIR

# instala requirements segun entorno (dev, prod, test)
ADD requirements/base.txt $WEBAPP_DIR/
ADD requirements/$DJANGO_ENV.txt $WEBAPP_DIR/

RUN pip install -r $DJANGO_ENV.txt

ADD . $WEBAPP_DIR/