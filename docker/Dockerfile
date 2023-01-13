FROM arm64v8/ubuntu:latest

RUN  apt-get update \
  && apt-get install -y wget \
  && rm -rf /var/lib/apt/lists/*

RUN wget https://github.com/graalvm/graalvm-ce-builds/releases/download/vm-22.3.0/graalvm-ce-java19-linux-aarch64-22.3.0.tar.gz

RUN tar -xzf graalvm-ce-java19-linux-aarch64-22.3.0.tar.gz
RUN rm graalvm-ce-java19-linux-aarch64-22.3.0.tar.gz

ENV PATH "/graalvm-ce-java19-22.3.0/bin:$PATH"

ENV JAVA_HOME "/graalvm-ce-java19-22.3.0"

RUN gu install native-image

ENTRYPOINT "/bin/sh"
