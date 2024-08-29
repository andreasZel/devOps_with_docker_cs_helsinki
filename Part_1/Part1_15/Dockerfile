FROM ubuntu:22.04

EXPOSE 8080

WORKDIR /usr/src/app

RUN apt-get update; \
apt-get install -y curl gnupg; \
curl -sL https://deb.nodesource.com/setup_16.x | bash -; \
apt-get install -y nodejs; \ 
apt-get install npm -y; \
rm -rf /var/lib/apt/lists/*

COPY . .

RUN npm install -f

RUN npm run build

CMD [ "npm", "run", "dev" ]