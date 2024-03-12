FROM node:18-alpine

WORKDIR /app

COPY frontend/trading-bot-v3/package.json ./
 
RUN npm install

COPY . .

RUN npm ci --quiet && npm run build

EXPOSE 8080

CMD [ "npm", "run", "preview" ]
