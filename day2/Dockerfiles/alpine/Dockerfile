FROM alpine:3.18
RUN apk add --no-cache nginx curl
EXPOSE 80
COPY index.html /var/www/html/
RUN ls -l /var/www/html/
WORKDIR /var/www/html
RUN mkdir -p /run/nginx
ENTRYPOINT ["nginx", "-g", "daemon off;"]
HEALTHCHECK --timeout=2s CMD curl -f localhost || exit 1
