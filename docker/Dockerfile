FROM ubuntu:14.04
RUN apt-get update && apt-get -y upgrade
RUN apt-get -y install java-1.8*
# Here comes the tomcat installation
RUN apt-get -y install tomcat7
RUN echo "JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto.x86_64" >> /etc/default/tomcat7

# Expose the default tomcat port
EXPOSE 8080

# Start the tomcat (and leave it hanging)
CMD service tomcat7 start && tail -f /var/lib/tomcat7/logs/catalina.out
