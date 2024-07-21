FROM node:18-alpine

WORKDIR /app

COPY server /app/server

WORKDIR /app/server

RUN npm install --force
WORKDIR /app

COPY client /app/client

WORKDIR /app/client
RUN npm install --force

RUN npm run build

WORKDIR /app/server

EXPOSE 4000

ENTRYPOINT ["node"]
CMD ["server.js"]