FROM nginx:1.16.1-alpine

RUN apk add --no-cache openssl bash

ENV DOCKERIZE_VERSION v0.6.1
RUN wget https://github.com/jwilder/dockerize/releases/download/$DOCKERIZE_VERSION/dockerize-alpine-linux-amd64-$DOCKERIZE_VERSION.tar.gz \
    && tar -C /usr/local/bin -xzvf dockerize-alpine-linux-amd64-$DOCKERIZE_VERSION.tar.gz \
    && rm dockerize-alpine-linux-amd64-$DOCKERIZE_VERSION.tar.gz

RUN rm /etc/nginx/conf.d/default.conf

#COPY ./nginx.tmpl /etc/nginx/conf.d
#RUN dockerize -template /etc/nginx/conf.d/nginx.tmpl:/etc/nginx/conf.d/nginx.conf

#COPY ./nginx.conf /etc/nginx/conf.d
