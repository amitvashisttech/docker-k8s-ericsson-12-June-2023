# Base Image
FROM ubuntu

# Update the APT Repo
RUN apt-get update 

# Install Apache Packages 
RUN apt-get install apache2 -y 

# Deploy Custom WebPage
COPY index.html  /var/www/html/info.html

# Bring up Apache App. 
CMD [ "/usr/sbin/apache2ctl", "-D", "FOREGROUND" ]