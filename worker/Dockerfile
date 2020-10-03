FROM node:alpine

WORKDIR /var/worker
COPY ./package.json ./
RUN npm install

COPY . .

CMD ["npm","run","start"]