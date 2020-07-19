FROM nginx:1.15.12-alpine

#<<<alpine>>> set timezone to JST
RUN apk --update --no-cache add tzdata && \
    cp /usr/share/zoneinfo/Asia/Tokyo /etc/localtime && \
    apk del tzdata

RUN apk add --update coreutils openssh-client certbot && rm -rf /var/cache/apk/*


ADD nginx.conf /etc/nginx/nginx.conf

RUN mkdir /etc/nginx/sites-enabled/
RUN mkdir /etc/nginx/cert
