# Pull base image.
FROM ubuntu:18.04
MAINTAINER HMF Team
# Install.
RUN  apt-get update && apt-get install -y \
    build-essential \
    software-properties-common \
    tar \
    vim \
    wget \
    curl \
    openssh-client \
    openssh-server \
    zlib1g-dev
# Install Java 8
RUN \
  echo oracle-java8-installer shared/accepted-oracle-license-v1-1 select true | debconf-set-selections && \
  apt-get update && \
  apt-get install -y openjdk-8-jre && \
  rm -rf /var/lib/apt/lists/*
ENV JAVA_HOME=/usr/lib/jvm/java-8-openjdk-amd64
ADD target/dcc-portal-server-5.2.13-SNAPSHOT.jar /opt/
