FROM node:8

RUN mkdir /poll
WORKDIR /poll
COPY package.json /poll/
RUN npm install
COPY . /poll/
EXPOSE 80
CMD node server.js
