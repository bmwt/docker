FROM ubuntu:bionic
RUN apt-get update \
 && apt-get upgrade -y \
 && apt-get install -y --no-install-recommends libssl1.0.0 \
    curl libssl-dev ca-certificates procps wget unzip vim joe \
 && rm -rf /var/lib/apt/lists/* \
 && mkdir /home/minecraft \
 && wget -O /home/minecraft/bedrock.zip https://minecraft.azureedge.net/bin-linux/bedrock-server-1.6.1.0.zip \
 && cd /home/minecraft; unzip /home/minecraft/bedrock.zip

USER root
COPY bedrock-entrypoint.sh /entrypoint.sh
# EXPOSE 19132:19132/udp
ENTRYPOINT "/entrypoint.sh"
