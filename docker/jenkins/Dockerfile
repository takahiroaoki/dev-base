FROM jenkins/jenkins:2.391

USER root

# install docker, docker-compose
ENV DOCKER_VERSION 20.10.10
RUN curl -fL -o docker.tgz "https://download.docker.com/linux/static/test/x86_64/docker-$DOCKER_VERSION.tgz" && \
    tar --strip-component=1 -xvaf docker.tgz -C /usr/bin

ENV DOCKER_COMPOSE_VERSION 1.29.2
RUN curl -L https://github.com/docker/compose/releases/download/${DOCKER_COMPOSE_VERSION}/docker-compose-`uname -s`-`uname -m` > /usr/local/bin/docker-compose && chmod +x /usr/local/bin/docker-compose