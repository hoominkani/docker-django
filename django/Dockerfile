FROM python:3.7
MAINTAINER hooomin <kanichan22@outlook.jp>
ENV PYTHONUNBUFFERED 1

ENV APP_PATH /opt/apps

COPY . $APP_PATH/
RUN pip install --no-cache-dir -r $APP_PATH/requirements.txt

# Package install
RUN apt-get update && apt-get -y install vim

WORKDIR $APP_PATH
RUN python manage.py collectstatic --noinput
