FROM        jianghang8421/prom-busybox:uclibc-arm64-support
MAINTAINER  The Prometheus Authors <prometheus-developers@googlegroups.com>

COPY prometheus                             /bin/prometheus
COPY promtool                               /bin/promtool
COPY prometheus.yml  /etc/prometheus/prometheus.yml
COPY console_libraries/                     /etc/prometheus/
COPY consoles/                              /etc/prometheus/

EXPOSE     9090
VOLUME     [ "/prometheus" ]
WORKDIR    /prometheus
ENTRYPOINT [ "/bin/prometheus" ]
CMD        [ "-config.file=/etc/prometheus/prometheus.yml", \
             "-storage.local.path=/prometheus", \
             "-web.console.libraries=/etc/prometheus/console_libraries", \
             "-web.console.templates=/etc/prometheus/consoles" ]