FROM ubuntu:16.04
RUN apt-get update \
  && apt-get install -y wget sudo \
  && wget -O - http://apt.llvm.org/llvm-snapshot.gpg.key|sudo apt-key add - \
  && echo "deb http://apt.llvm.org/xenial/ llvm-toolchain-xenial-4.0 main" > /etc/apt/sources.list.d/clang4.list \
  && apt-get update \
  && apt-get install -y \
  clang-4.0 \
  libboost-all-dev \
  gcc \
  g++ \
  git-core \
  && rm -rf /build/* \
  && rm -rf /tmp/* /var/tmp/* \
  && rm -rf /usr/share/doc/* \
  && rm -rf /var/lib/apt/lists/*
RUN ln -s /usr/bin/clang-4.0 /usr/bin/clang
RUN ln -s /usr/bin/clang-4.0 /usr/bin/clang-3.5
RUN ln -s /usr/bin/clang++-4.0 /usr/bin/clang++
RUN ln -s /usr/bin/clang++-4.0 /usr/bin/clang++-3.5
