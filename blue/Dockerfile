# Use nginx stable alpine image as the base image
FROM nginx:stable-alpine

# Remove the default nginx index page
RUN rm /usr/share/nginx/html/index.html

# Create a new index.html
RUN echo '<html>' > /usr/share/nginx/html/index.html
RUN echo '<body style="background-color:blue;">' >> /usr/share/nginx/html/index.html
RUN echo '<h1>Blue Server</h1>' >> /usr/share/nginx/html/index.html
RUN echo '<p>Service Name: blue-service</p>' >> /usr/share/nginx/html/index.html
RUN echo '<p>Node Name: $(hostname)</p>' >> /usr/share/nginx/html/index.html
RUN echo '</body>' >> /usr/share/nginx/html/index.html
RUN echo '</html>' >> /usr/share/nginx/html/index.html

# Expose port 80
EXPOSE 80

# Start nginx and keep it running
CMD ["nginx", "-g", "daemon off;"]

