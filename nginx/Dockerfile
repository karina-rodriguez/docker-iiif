# https://hub.docker.com/_/python
FROM ubuntu
RUN apt-get -y update && apt-get -y install nginx \
locate
EXPOSE 80/tcp

#copy whatever files we already have

COPY /nginx/htdocs/* /var/www/html/
#COPY /nginx/.conf /etc/nginx/conf.d/
#insert a CORS line to the config file of apache
COPY /nginx/default /etc/nginx/sites-available/
#COPY /nginx/default /etc/nginx/sites-enabled/
CMD ["/usr/sbin/nginx", "-g", "daemon off;"]
#RUN service nginx reload


