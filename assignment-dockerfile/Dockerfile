# fill in the blanks to dockerize this node app
FROM node:20-alpine3.19

EXPOSE 3000

RUN apk add --no-cache tini

WORKDIR '/usr/src/app'

COPY package.json package-lock.json* ./

RUN npm install && npm cache clean --force

COPY app.js .

# ENTRYPOINT ["tini", "--"]

CMD ["node", "app.js"]
