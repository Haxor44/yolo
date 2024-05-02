FROM node:20-alpine3.19 as build

WORKDIR /app

COPY package*.json ./

RUN npm install
RUN npm install -g npm@10.7.0

COPY . .

FROM node:20-alpine as prod

COPY --from=build /app ./

EXPOSE 3000

CMD [ "npm","start" ]
 