FROM node:24-alpine AS builder

WORKDIR /app

COPY package*.json /app/

RUN npm install

COPY . /app

FROM node:24-alpine

WORKDIR /app

COPY --from=builder /app/node_modules /app/node_modules
COPY . /app

CMD ["node", "index.js"]
