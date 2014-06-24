## sample python flask applicationi image


### Classic python web applicaiton:

> **User**

>> &darr;&darr; HTTP request

> **HTTP server: Nginx**

>> &darr;&darr; *HTTP reverse proxying & serves static files*

> **Web server: gunicorn**

>> &darr;&darr; *WSGI interface*

> **Web applicaiton: flask**


### Quick start: run the container
<pre>docker run -p 9999:80 feifan/flasksample</pre>
Application will start running on `localhost:9999` or `(boot2docker ip):9999`

#### Screen shot:
(boot2docker ip: 192.168.59.103)

![screen shot](Screenshot.png)


