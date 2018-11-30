FROM        jianghang8421/prom-busybox:uclibc-arm64-support
MAINTAINER  The Prometheus Authors <prometheus-developers@googlegroups.com>

COPY amtool                     /bin/amtool
COPY alertmanager               /bin/alertmanager
COPY simple.yml    /etc/alertmanager/config.yml

EXPOSE     9093
VOLUME     [ "/alertmanager" ]
WORKDIR    /alertmanager
ENTRYPOINT [ "/bin/alertmanager" ]
CMD        [ "--config.file=/etc/alertmanager/config.yml", \
             "--storage.path=/alertmanager" ]