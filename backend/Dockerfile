FROM node:13-alpine as build

WORKDIR /app

COPY package*.json ./

RUN npm install

COPY . .

FROM build

EXPOSE 5000

CMD [ "npm","start" ]
