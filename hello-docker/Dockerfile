FROM node:18-alpine/node

WORKDIR /app

COPY package*.json ./ /app/

RUN npn nstall 

COPY . .

CMD ["npm", "start"]