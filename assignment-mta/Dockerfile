FROM node:18

# Not working
# RUN apt-get update && apt-get install -y graphicsmagick

WORKDIR /app

COPY package*.json ./

RUN npm install && npm cache clean --force

COPY . .

ENV CHARCOAL_FACTOR=0.1

CMD ["node", "index.js"]
