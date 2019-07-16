#Using node as our base for the image
FROM node:latest

#Setting our working dir to /app

WORKDIR /app

#Updating apt

RUN apt-get update

#adding dir path to PATH

ENV PATH /app/node_modules/.bin:$PATH

COPY package.json /app
RUN NG_CLI_ANALYTICS=ci npm install
RUN NGI_CLI_ANALYTICS=ci npm install -g @angular/cli

COPY . /app

CMD ng serve --host 0.0.0.0

EXPOSE 4200
