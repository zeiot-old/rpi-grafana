# VERSION 5.0.0
# AUTHOR:         Nicolas Lamirault <nicolas.lamirault@gmail.com>
# DESCRIPTION:    zeiot/rpi-grafana

FROM resin/armv7hf-debian:stretch
MAINTAINER Nicolas Lamirault <nicolas.lamirault@gmail.com>

ENV GRAFANA_VERSION 5.0.0

RUN apt-get update && \
    apt-get install libfontconfig

ADD https://github.com/fg2it/grafana-on-raspberry/releases/download/v${GRAFANA_VERSION}/grafana-${GRAFANA_VERSION}.linux-armhf.tar.gz /grafana.tar.gz
RUN tar -xf /grafana.tar.gz \
    && rm /grafana.tar.gz \
    && mv /grafana-${GRAFANA_VERSION} /grafana

EXPOSE 3000

VOLUME ["/data", "/etc/grafana"]

CMD /grafana/bin/grafana-server --homepath=/grafana --config=/etc/grafana/grafana.ini
