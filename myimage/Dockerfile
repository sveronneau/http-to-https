FROM alpine:3.8

RUN apk --update --no-cache add nginx
RUN mkdir /var/lib/nginx/html
RUN touch /var/lib/nginx/html/check.html

COPY global.conf /etc/nginx/modules/global.conf
COPY http.conf /etc/nginx/conf.d/default.conf

EXPOSE 80

CMD /usr/sbin/nginx
