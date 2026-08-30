FROM node:24-alpine AS builder

WORKDIR /app

COPY package*.json /app

# npm install will install the dependencies in node_modules directory
RUN npm install

COPY . /app


#npm run build will store the output in /build folder
RUN npm run build

FROM nginx:alpine

RUN rm -rf /usr/share/nginx/html/*

COPY --from=builder /app/build /usr/share/nginx/html

COPY nginx.conf /etc/nginx/nginx.conf

CMD ["nginx", "-g", "daemon off;"]
