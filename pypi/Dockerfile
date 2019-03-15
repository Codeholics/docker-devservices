FROM python:alpine
ARG WORKERS
ENV WORKERS 2
ARG PORT
ENV PORT 8675

RUN apk update && apk upgrade &&\
  pip install gunicorn pypiserver &&\
  mkdir /packages
CMD /usr/local/bin/gunicorn --access-logfile "-" --workers $WORKERS --bind 0.0.0.0:$PORT 'pypiserver:app(root="/packages", authenticated=None)'
