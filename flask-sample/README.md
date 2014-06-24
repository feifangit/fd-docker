## sample python flask applicationi image

### Quick start: run the container
<pre>docker run -p 9999:80 feifan/flasksample</pre>
Application will start running on `localhost:9999` or `(boot2docker ip):9999`

#### Screen shot:
(boot2docker ip: 192.168.59.103)

![screen shot](Screenshot.png)


### Run on Amazon Elastic Beanstalk
upload `Dockerrun.aws.json` in the project to AWS elastic beanstalk console. It takes about 8~10 minutes to finish the deployment.
![screen shot](Screenshot2.png)

<iframe width="420" height="315" src="//www.youtube.com/embed/lBu7Ov3Rt-M" frameborder="0" allowfullscreen></iframe>

