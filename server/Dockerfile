FROM node:alpine

WORKDIR /var/server

COPY ./package.json ./
RUN npm install
COPY . .

CMD ["npm","run","start"] 