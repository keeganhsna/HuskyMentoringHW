FROM ubuntu:20.04

# From /etc/lsb-release
ARG DISTRIB_ID=ubuntu
ARG DISTRIB_CODENAME=focal

RUN apt-get update && \
  apt-get install -y \
    curl \
    gnupg \
    net-tools \
    netcat

# To install Telegraf, we need to add the Influxdata package repos.
RUN curl -s https://repos.influxdata.com/influxdb.key | apt-key add -
RUN echo "deb https://repos.influxdata.com/$DISTRIB_ID $DISTRIB_CODENAME stable" | tee /etc/apt/sources.list.d/influxdb.list && \
  apt-get update && \
  apt-get install -y telegraf

CMD ["bash"]
