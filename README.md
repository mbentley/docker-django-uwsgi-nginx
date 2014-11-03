mbentley/django-uwsgi-nginx
==================

docker image for django (uwsgi) & nginx
based off of stackbrew/debian:jessie

To pull this image:
`docker pull mbentley/django-uwsgi-nginx`

Example usage:
`docker run -p 80 -d -e MODULE=myapp mbentley/django-uwsgi-nginx`

You can mount the application volume to run a specific application.  The default volume inside in the container is `/opt/django/app`.  Here is an example:
`docker run -p 80 -d -e MODULE=myapp -v /home/mbentley/myapp:/opt/django/app mbentley/django-uwsgi-nginx`

By default, this just runs a default 'welcome to django' project.
