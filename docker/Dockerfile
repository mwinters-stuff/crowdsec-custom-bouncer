FROM ubuntu:latest
# RUN apk add bash
RUN apt-get update && apt-get -y install wget
WORKDIR /provision
RUN wget https://github.com/crowdsecurity/cs-custom-bouncer/releases/download/v0.0.11/crowdsec-custom-bouncer.tgz
RUN tar xzvf crowdsec-custom-bouncer.tgz --strip-components=1
RUN ls -l
RUN cp crowdsec-custom-bouncer /usr/bin/ 
RUN ls -l /usr/bin
ENTRYPOINT [ "crowdsec-custom-bouncer", "-c", "/config/crowdsec-custom-bouncer.yaml" ]
