# Build Stage
FROM node:18-alpine as build
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .

# Final lightweight image
FROM node:18-alpine
WORKDIR /app
COPY --from=build /app .
EXPOSE 5000
C["npm", "start"]
