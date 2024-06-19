# Use the official NGINX image as base
FROM nginx

# Metadata
LABEL "Project"="Vprofile"
LABEL "Author"="Nixx"

# Remove default NGINX configuration
RUN rm -rf /etc/nginx/conf.d/default.conf

# Copy custom NGINX configuration
COPY nginvproapp.conf /etc/nginx/conf.d/vproapp.conf
