FROM nginx

RUN apt update
RUN apt install -y vim

COPY webapp /usr/share/nginx/html
COPY conf/nginx.conf /etc/nginx/conf.d/default.conf

ENTRYPOINT [ "nginx", "-g", "daemon off;" ]

# CMD [ "" ]