FROM node:18-alpine

WORKDIR /app

COPY package*.json ./
RUN npm install

COPY . .

RUN npm run build

# Use a static file server
RUN npm install -g serve

EXPOSE 4173

CMD ["serve", "-s", "dist"]
