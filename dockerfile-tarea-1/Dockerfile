FROM node:6.17.1-alpine AS firstDocker

WORKDIR /usr/src/app
COPY package.json /usr/src/app/
COPY . /usr/src/app

RUN npm install \
&& cache clean --force \

EXPOSE 3000

CMD ["/sbin/tini","--" ,"node", "./bin/www"]
