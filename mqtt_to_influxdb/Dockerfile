FROM ubuntu:bionic
RUN apt-get update \
 && apt-get upgrade -y \
 && apt-get install -y --no-install-recommends libssl1.0.0 \
    curl libssl-dev ca-certificates procps wget joe \
 && rm -rf /var/lib/apt/lists/* \
 && wget -O /mqtt_to_influxdb.py https://github.com/bmwt/python/raw/master/mqtt_to_influxdb.py

USER root
ENTRYPOINT "/mqtt_to_influxdb.py"
