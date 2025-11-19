#
# Dockerfile for python
#

FROM gcr.io/google.com/cloudsdktool/cloud-sdk:slim

RUN apt-get update && apt-get install -y build-essential libssl-dev zlib1g-dev \
 libbz2-dev libreadline-dev libsqlite3-dev wget curl llvm libncurses5-dev libncursesw5-dev \
 xz-utils tk-dev libffi-dev liblzma-dev python3-openssl git
RUN git clone --depth 1 --branch v2.6.12 https://github.com/pyenv/pyenv.git .pyenv

ENV PYENV_ROOT=$HOME/.pyenv
ENV PATH=$PYENV_ROOT/shims:$PYENV_ROOT/bin:$PATH
RUN pyenv install 3.13.5
