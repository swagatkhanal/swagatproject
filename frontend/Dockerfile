FROM nginx:alpine
# Copy your custom config to the Nginx config directory
COPY nginx.conf /etc/nginx/conf.d/default.conf
# Copy the single HTML file
COPY index.html /usr/share/nginx/html/index.html
EXPOSE 80
