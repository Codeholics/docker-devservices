FROM jenkins/jenkins:lts-alpine
USER root
RUN apk update \
 && apk upgrade \
 && apk add \
     make gcc python3 python3-dev musl-dev \
     openssl-dev libzip readline \ 
 && pip3 install --upgrade pip tox pytest flake8 pylint

USER jenkins
