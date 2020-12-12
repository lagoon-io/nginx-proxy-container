FROM nginx:1.19

ARG DEV_PACKAGES="vim"

COPY ./config/conf.d/server.conf /etc/nginx/conf.d/server.conf
COPY ./config/ssl/server.crt /etc/nginx/conf.d/server.crt
COPY ./config/ssl/server.key /etc/nginx/conf.d/server.key

RUN apt-get update -y && \
  apt-get install -y ${DEV_PACKAGES} && \
  chmod 644 /etc/nginx/conf.d/server.crt && \
  chmod 644 /etc/nginx/conf.d/server.key
