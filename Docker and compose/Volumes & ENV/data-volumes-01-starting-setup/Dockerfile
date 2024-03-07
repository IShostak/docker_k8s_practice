FROM node:latest

WORKDIR /app

COPY package.json .

RUN npm install

COPY . .

EXPOSE 80

ARG DEF_PORT=80

ENV PORT=$DEF_PORT \
    ENV_VAL2 = 'val'

EXPOSE $PORT, $ENV_VAL2

VOLUME ["/app/feedback"]

CMD ["node", "server.js"]