FROM node:18-alpine

WORKDIR /app

COPY frontend/trading-bot-v3/package.json ./

# Install dependencies
RUN npm install

# Copy the rest of the application code
COPY . .

# Install production dependencies
RUN npm ci --quiet

# Build the project
RUN npm run build

EXPOSE 8080

CMD ["npm", "run", "preview"]
