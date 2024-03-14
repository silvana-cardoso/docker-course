FROM node:14

WORKDIR /app

COPY package.json .

RUN npm install

COPY . .

EXPOSE 80

# UNSUCCESSFUL TRY
# path inside of the container, which
# should map to a folder outside of the container
# VOLUME [ "/app/feedback" ]

CMD [ "node", "server.js" ]
