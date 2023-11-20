FROM golang:1.21-bullseye

RUN apt-get update && \
    apt-get install -y protobuf-compiler && \
    apt-get install -y software-properties-common apt-transport-https ca-certificates gnupg2 curl build-essential

RUN curl -sL https://deb.nodesource.com/setup_20.x | bash - && \
    apt-get install -y nodejs && \
    npm install -g npm@10.2.4

RUN useradd -ms /bin/bash vanio

RUN npm install -g serverless && \
    npm install -g serverless-offline

WORKDIR /app

CMD tail -f /dev/null