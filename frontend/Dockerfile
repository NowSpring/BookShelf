FROM node:21-alpine3.18

WORKDIR /src
COPY trainpad/package.json trainpad/package-lock.json ./
RUN npm install -g npm@latest && npm install -g vite@latest
