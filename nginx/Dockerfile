FROM debian:jessie

MAINTAINER Sandor Farkas <farkas.berlin@gmail.com>

RUN apt-get update && apt-get install -y \
    nginx

ADD nginx.conf /etc/nginx/
ADD sites-available/* /etc/nginx/sites-available/

#make this dynamic
RUN ln -s /etc/nginx/sites-available/projectA.conf /etc/nginx/sites-enabled/projectA \
&& rm /etc/nginx/sites-enabled/default

RUN echo "upstream php-upstream { server php:9000; }" > /etc/nginx/conf.d/upstream.conf

RUN usermod -u 1000 www-data

CMD ["nginx"]

EXPOSE 80
EXPOSE 443
