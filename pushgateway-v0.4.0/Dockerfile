FROM        jianghang8421/prom-busybox:uclibc-arm64-support
MAINTAINER  The Prometheus Authors <prometheus-developers@googlegroups.com>

COPY pushgateway /bin/pushgateway

EXPOSE     9091
WORKDIR    /pushgateway
ENTRYPOINT [ "/bin/pushgateway" ]