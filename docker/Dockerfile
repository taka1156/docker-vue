FROM node:14.15.1-alpine3.10

WORKDIR /usr/src/app

RUN apk update && \
    apk add git && \
    npm install -g npm @vue/cli@ @vue/cli-init \
    npm install -g @gridsome/cli \
    npm install -g create-nuxt-app@2.15.0 \
    npm install -g firebase-tools \
