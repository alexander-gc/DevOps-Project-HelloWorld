FROM ubuntu

RUN apt-get update -y \
    && apt-get upgrade -y \
    && apt-get install -y \
    nodejs \
    npm

WORKDIR /app

COPY package*.json ./

RUN npm install

COPY . .

#RUN npm run build

ENV PORT=3000

EXPOSE ${PORT}

CMD ["npm", "start"]
