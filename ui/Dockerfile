FROM node:latest
WORKDIR /app
COPY package.json ./
RUN npm install -g @vue/cli
COPY . .
EXPOSE 3000
CMD ["npm", "start"]
