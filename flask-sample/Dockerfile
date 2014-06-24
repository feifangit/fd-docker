FROM feifan/pywebapp

MAINTAINER FAN FEI(feifan.pub@gmail.com)

RUN apt-get update

# install python libraries
ADD requirements.txt /tmp/
RUN pip install -r /tmp/requirements.txt

# install supervisord config
ADD flaskapp.conf /etc/supervisor/conf.d/flaskapp.conf

# config nginx
RUN rm -f /etc/nginx/sites-enabled/default
ADD ngx_webapp /etc/nginx/sites-enabled/

# copy web app 
ADD flaskapp /var/www/flaskapp
RUN chmod -R +r /var/www/flaskapp
