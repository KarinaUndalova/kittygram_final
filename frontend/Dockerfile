FROM node:18
WORKDIR /app

COPY ["package.json", "package-lock.json*", "./"]

RUN npm ci

COPY . .

RUN npm run build && npm install --global http-server

CMD ["npx", "-y", "http-server", "-p", "8080", "/app/build"]
