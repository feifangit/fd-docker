## docker image feifan/pywebapp
basic container for python web application. based on `feifan/supervisord`

Includes:
>
 1. latest stable version nginx
 2. compile tools: 
    * gcc
    * python-dev
 3. web server & tools:
    * gunicorn 
    * gevent
 4. python library tools:
    * pip
 5. /var/www folder 


### get this image
`docker pull feifan/pywebapp`

### start a container
`docker run -p 8888:80 feifan/pywebapp`

### access container
<pre>curl http://localhost:8888 </pre>
(on Mac OS, the IP is `boot2docker ip` instead of `localhost`)

you will get the default nginx page
