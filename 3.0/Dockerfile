# VERSION 3.0.4
# AUTHOR:         Nicolas Lamirault <nicolas.lamirault@gmail.com>
# DESCRIPTION:    zeiot/rpi-grafana

FROM resin/armv7hf-debian:jessie
MAINTAINER Nicolas Lamirault <nicolas.lamirault@gmail.com>

ENV GRAFANA_VERSION 3.0.4
ENV GRAFANA_SUFFIX 1464784925

RUN apt-get update && \
    apt-get install libfontconfig

ADD https://github.com/heziegl/rpi-grafana-build/raw/master/dist-${GRAFANA_VERSION}/grafana-${GRAFANA_VERSION}-${GRAFANA_SUFFIX}.linux-arm.tar.gz /grafana.tar.gz

RUN tar -xf /grafana.tar.gz \
    && rm /grafana.tar.gz \
    && mv /grafana-${GRAFANA_VERSION}-${GRAFANA_SUFFIX} /grafana

EXPOSE 3000

VOLUME ["/var/lib/grafana", "/etc/grafana"]

CMD /grafana/bin/grafana-server --homepath=/grafana --config=/etc/grafana/grafana.ini
