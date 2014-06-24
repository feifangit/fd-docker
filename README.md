## Basic images for python web application

### [feifan/supervisord](https://registry.hub.docker.com/u/feifan/supervisord/)
very basic image, includes supervisord, a process management service.[detail](./supervisord/README.md)

### [feifan/pywebapp](https://registry.hub.docker.com/u/feifan/pywebapp/)
a platform to run python applications. Nginx, gunicorn, gevent inside.[detail](./pywebapp/README.md)

based on `feifan/supervisord`


### [feifan/flasksample](https://registry.hub.docker.com/u/feifan/flasksample/)
a flask web application deployed in classic hierarchy.[detail](./flaskapp/README.md)

based on `feifan/pywebapp`

> **User**

>> &darr;&darr; HTTP request

> **HTTP server: Nginx**

>> &darr;&darr; *HTTP reverse proxying & serves static files*

> **Web server: gunicorn**

>> &darr;&darr; *WSGI interface*

> **Web applicaiton: flask**