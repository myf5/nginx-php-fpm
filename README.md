# Nginx+php-fpm+chacha20+cert transparency+memcached+brotli+tls dynamic record+wordpress
##This docker file is used to build a docker image runs:
nginx  1.12.1
php-fpm 5.6.31
Based on php:5.6.31-fpm-alpine
##Also support:
ssl:chacha20_poly1305
certificate transparency 1.3.2
Brotli 1.0.2
TLS dynamic record sizing patch
memcached

##It is used for my wordress environment. 
So if you want to build yours on this dockerfile, you may need change related conf file and certificates and anything that different to  you environment.
