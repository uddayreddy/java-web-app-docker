from maven:3.5.3-jdk-8

RUN apt-get update -y \
 && apt-get install -y apt-utils \
 && apt-get install -y apt-transport-https dirmngr \
 && echo 'deb https://apt.dockerproject.org/repo debian-stretch main' >> /etc/apt/sources.list \
 && apt-key adv --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 58118E89F3A912897C070ADBF76221572C52609D \
 && apt-get update \
 && apt-get install -y docker-engine \
 && curl -L https://github.com/docker/compose/releases/download/1.21.1/docker-compose-$(uname -s)-$(uname -m) -o /usr/local/bin/docker-compose \
 && chmod +x /usr/local/bin/docker-compose

CMD ["mvn"]

