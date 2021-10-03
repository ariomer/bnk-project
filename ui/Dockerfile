FROM node:latest
WORKDIR /app
COPY package.json ./
RUN npm install -g npm@7.24.1
COPY . .
EXPOSE 3000
CMD ["npm", "start"]
