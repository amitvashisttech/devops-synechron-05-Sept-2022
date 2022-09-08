# Jenkins Deployment & Configuration


### First you have to be Super User : root
```
sudo su - 
```

### Download Jenkins & Install Java JDK
```
  apt-get update; apt-get install default-jdk -y
  java -version
  wget https://get.jenkins.io/war-stable/2.346.2/jenkins.war 
  mv jenkins.war /root/
```


### Setup Jenkins to run on custom port : 9090
```
nohup  java -jar /root/jenkins.war --httpPort=9090 > output.txt & 
```

### Now you can access the Jenkins via Web Brower, Please go ahead & Complete the Setup process 


### Get the initial Credentials
```
 cat /root/.jenkins/secrets/initialAdminPassword
```


