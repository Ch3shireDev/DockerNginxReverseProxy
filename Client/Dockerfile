FROM node:14.2.0-alpine3.11 as build
WORKDIR /app
COPY . .
FROM nginx as runtime
COPY --from=build /app/ /usr/share/nginx/html
EXPOSE 80