FROM node:22-bookworm-slim

COPY legal-app/ /app
WORKDIR /app

RUN rm -rf "app/(example)"
RUN npm ci
RUN npm i sharp
RUN npm run build

EXPOSE 3000

ENTRYPOINT [ "npm", "start" ]