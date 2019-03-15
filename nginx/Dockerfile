FROM nginx:alpine
RUN apk update && \
  apk upgrade && apk add openssl apache2-utils
COPY ./conf.d/default.conf /etc/nginx/conf.d/default.conf
COPY ./certs/* /certs/
RUN htpasswd -b -c /etc/nginx/htpasswd root test123
