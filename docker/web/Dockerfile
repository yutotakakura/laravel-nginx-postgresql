FROM nginx:1.25-alpine

ENV TZ=UTC

COPY ./docker/web/*.conf /etc/nginx/conf.d/

WORKDIR /var/www/html