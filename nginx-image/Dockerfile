#imagename:imagetage (founded in my machine)
FROM centos:centos7   
LABEL maintainer="Shady Salah <shady.salah@unknown.com>"

RUN yum install -y wget openssl sed &&\
    yum -y autoremove &&\
    yum clean all &&\
    wget  http://nginx.org/packages/centos/7/x86_64/RPMS/nginx-1.14.0-1.el7_4.ngx.x86_64.rpm &&\
    rpm -iv nginx-1.14.0-1.el7_4.ngx.x86_64.rpm

COPY nginx.conf /etc/nginx/nginx.conf
COPY index.html /data/www/index.html
VOLUME [ "/data/www" ]
EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]


