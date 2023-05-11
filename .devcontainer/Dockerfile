ARG UBUNTU_VERSION=22.04

FROM ubuntu:${UBUNTU_VERSION}

RUN apt-get update && \
    apt-get upgrade -y && \
    apt-get install -y git

RUN apt-get install -y ruby ruby-dev gcc make postgresql-server-dev-all

RUN gem install bundler -v 2.3.26

ENV RUBYLIB=/workspace/lib/

RUN echo 'postgresql:5432:sensu_test_db:sensu_test_user:pass\:word' > /tmp/pgpass_escaped
RUN echo 'postgresql:5432:sensu_test_db:sensu_test_user:pass:word' > /tmp/pgpass
