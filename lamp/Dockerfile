# Pull base image.
FROM ubuntu:16.04

# Install Nginx, Mariadb, Php
RUN \
# add the repository of Nginx
  deb http://nginx.org/packages/ubuntu/ xenial nginx \
  deb-src http://nginx.org/packages/ubuntu/ xenial nginx \
# add the repository of Mariadb
  apt-get install software-properties-common 
  apt-key adv --recv-keys --keyserver hkp://keyserver.ubuntu.com:80 0xcbcb082a1bb943db 
  add-apt-repository 'deb http://ftp.osuosl.org/pub/mariadb/repo/10.0/ubuntu trusty main
  apt-get update && \
  apt-get install -y nginx && mariadb-server && php7.0 \
  rm -rf /var/lib/apt/lists/* && \
  echo "\ndaemon off;" >> /etc/nginx/nginx.conf && \
  chown -R www-data:www-data /var/lib/nginx

# Define mountable directories.
VOLUME ["/etc/nginx/sites-enabled", "/etc/nginx/certs", "/etc/nginx/conf.d", "/var/log/nginx", "/var/www/html"]

# Define working directory.
WORKDIR /etc/nginx
