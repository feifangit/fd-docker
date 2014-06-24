## docker image feifan/supervisord
Includes:
>
 1. supervisord and set as auto starup
 2. SSH service: 
    * username/password: root/futureDial1

Images based on it should put its own *.conf `supervisord` config file under `/etc/supervisor/conf.d/`

### get this image
`docker pull feifan/supervisord`

### start container
<pre>
docker run -p 2222:22 feifan/supervisord
</pre>

### access SSH service
<pre>
ssh -p 2222 root@localhost
</pre>
(on Mac OS, the IP is `boot2docker ip` instead of `localhost`)