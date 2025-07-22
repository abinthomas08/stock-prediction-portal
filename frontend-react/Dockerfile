# frontend-react/Dockerfile
FROM node:18-alpine

WORKDIR /app

COPY frontend-react/package*.json ./
RUN npm install

COPY frontend-react .

RUN npm run build

# Optional: use a dev server instead of build
# CMD ["npm", "run", "dev"]
