FROM node

# by defining the work directory we can use the second directory in COPY command as just "./ " instead of "/app"
WORKDIR /app

COPY package.json /app

RUN npm install
# copy the packages and install the dependencies separatly to save time when updating the source code

COPY . /app 

EXPOSE 80

CMD ["node", "server.js"]