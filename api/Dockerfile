FROM node:11-alpine

WORKDIR /usr/src/app

COPY package*.json .
RUN npm install --prod

COPY . .

ENV API_PORT=3000

EXPOSE $API_PORT
HEALTHCHECK CMD curl --fail http://localhost:$API_PORT/api/status || exit 1
CMD ["npm", "start"]
