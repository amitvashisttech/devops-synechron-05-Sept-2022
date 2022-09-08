# Use Tomcat RunTime Image 

#FROM tomcat:9.0.65-jre11
FROM tomcat:8.0 

MAINTAINER Amit Vashist <amitvashist7@gmail.com>

RUN mkdir -p /usr/local/tomcat/webapps/jenkins

COPY target/petclinic.war /usr/local/tomcat/webapps/

COPY index.html /usr/local/tomcat/webapps/jenkins/
