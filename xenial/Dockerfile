# PyEnv on Ubuntu 16.04 (Xenial)
# VERSION               0.1

FROM ubuntu:16.04
MAINTAINER John Vrbanac <john.vrbanac@linux.com>

RUN apt-get update
RUN DEBIAN_FRONTEND=noninteractive apt-get -y install git make build-essential python-dev python-pip libssl-dev zlib1g-dev libbz2-dev libreadline-dev libsqlite3-dev curl

RUN git clone git://github.com/yyuu/pyenv.git .pyenv
RUN git clone https://github.com/yyuu/pyenv-virtualenv.git ~/.pyenv/plugins/pyenv-virtualenv

ENV HOME  /
ENV PYENV_ROOT $HOME/.pyenv
ENV PATH $PYENV_ROOT/shims:$PYENV_ROOT/bin:$PATH

RUN pyenv install 2.7.12
RUN pyenv install 3.4.5
RUN pyenv install pypy2-5.4.1

RUN pyenv global 2.7.12 3.4.5 pypy2-5.4.1
