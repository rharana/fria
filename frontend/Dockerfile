FROM node:18-slim

WORKDIR /usr/src/app

COPY ./package.json .
COPY ./package-lock.json .

RUN npm install

COPY . .

CMD ["npm", "run", "dev-exposed"]
