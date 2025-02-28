FROM node:14

# Make current folder working directory
WORKDIR /app

COPY package*.json ./

# Install project dependecies
RUN npm install

COPY . .

EXPOSE 8080

CMD [ "npm", "run", "dev" ]
