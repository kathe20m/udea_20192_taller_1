FROM node:6.17.1-alpine AS firstDocker

WORKDIR /usr/src/app
COPY package.json /usr/src/app/
COPY . /usr/src/app

RUN apk add --update tini \
&& npm install \
&& npm cache clean --force

EXPOSE 3000

ENTRYPOINT ["/sbin/tini", "--"]

CMD ["node", "./bin/www"]

