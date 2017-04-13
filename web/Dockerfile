# Base Image
FROM ubuntu

# Passed arguments
ARG DIR

# Install Nginx
RUN apt-get update
RUN apt-get -y install nginx

# Configure Nginx
RUN rm /etc/nginx/sites-enabled/default
COPY vhost /etc/nginx/sites-enabled/default

# Set sites
RUN rm /var/www/html/index.*
COPY ${DIR}/index.html /var/www/html/index.html

# Install debugging utilities
# RUN apt-get -y install curl
# RUN apt-get -y install vim

# Start nginx in the foreground
CMD nginx -g "daemon off;"

# Expose port
EXPOSE 80
