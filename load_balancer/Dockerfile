# Base Image
FROM ubuntu

# Install Nginx
RUN apt-get update
RUN apt-get -y install nginx

# Configure Nginx
RUN rm /etc/nginx/nginx.conf
COPY nginx.conf /etc/nginx/nginx.conf

# Install debugging utilities
# RUN apt-get -y install curl
# RUN apt-get -y install vim

# Start nginx in the foreground
CMD nginx -g "daemon off;"

# Expose port
EXPOSE 80
