FROM nginx:alpine

# Copy static frontend files directly to the Nginx serving path
COPY . /usr/share/nginx/html

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]
