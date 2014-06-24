FROM feifan/supervisord

MAINTAINER FAN FEI(feifan.pub@gmail.com)


RUN apt-get update
RUN apt-get install -y python-setuptools python-software-properties software-properties-common
RUN easy_install pip
RUN add-apt-repository -y ppa:nginx/stable
RUN apt-get update

RUN apt-get install -y nginx-full gcc python-dev libevent-dev cython

# nginx run in non-daemon mode
RUN echo "daemon off;" >> /etc/nginx/nginx.conf

# start nginx by supervisord
ADD nginx.conf /etc/supervisor/conf.d/nginx.conf
RUN mkdir /var/www


ADD requirements.txt /tmp/
RUN pip install -r /tmp/requirements.txt