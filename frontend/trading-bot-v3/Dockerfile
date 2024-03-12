FROM node:14-alpine

WORKDIR /app

# Debugging
RUN npm -v
RUN ls -al

COPY package.json .
COPY package-lock.json .

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
