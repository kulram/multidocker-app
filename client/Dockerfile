FROM node:alpine

WORKDIR /var/app
COPY ./package.json ./
RUN npm install
COPY ./public ./public
COPY ./src ./src
RUN npm run build

FROM nginx:alpine
COPY ./nginx/default.conf /etc/nginx/conf.d/default.conf
COPY --from=0 /var/app/build /usr/share/nginx/html


