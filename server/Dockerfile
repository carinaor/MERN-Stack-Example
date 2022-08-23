FROM node:16-alpine

RUN apk update
RUN apk upgrade
RUN docker info

WORKDIR /app

COPY package.json ./
COPY server.js ./
COPY yarn.lock ./

ADD db /app/db
ADD routes /app/routes

RUN yarn install --production

CMD node server.js
