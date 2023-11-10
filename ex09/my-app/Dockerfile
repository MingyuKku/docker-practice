FROM node:alpine as build

WORKDIR /app

COPY package.json .

RUN npm install --silent

COPY . .

RUN npm run build


FROM nginx

COPY --from=build /app/build /usr/share/nginx/html

ENTRYPOINT [ "nginx", "-g", "daemon off;" ]