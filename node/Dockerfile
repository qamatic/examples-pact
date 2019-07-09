FROM node:10.15.3-alpine AS build

# install gyp tools
RUN apk update \
        && apk upgrade

RUN apk add --no-cache \
        python \
        make \
        g++ \
        && rm -rf /var/cache/apk/*

RUN npm i -g npm@6.9.0
RUN mkdir -p /examples-pact
COPY ./package.json /examples-pact
WORKDIR /examples-pact

RUN npm install
