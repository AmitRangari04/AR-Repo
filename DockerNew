# syntax=docker/dockerfile:1

FROM node:18-alpine
WORKDIR /app
COPY . .
RUN yarn install --production
CMD ["node", "src/index.js"]
EXPOSE 3000
FROM ubuntu
RUN apt-get update
RUN apt-get install nginx -y
COPY index.nginx-debian.html /var/www/html/
CMD ["nginx","-g","daemon off;"]
