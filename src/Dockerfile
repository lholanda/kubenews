FROM node:20.10.0-alpine3.19

HEALTHCHECK --interval=30s --timeout=30s --start-period=5s --retries=3 CMD [ "executable" ]

USER node
WORKDIR /app

# antes de copiar define proprietario do arquivo
COPY --chown=node:node package*.json .

RUN npm install 

#RUN npm install --save mysql2

COPY --chown=node:node . .

# requsito do projeto - server.js
EXPOSE 8080

CMD [ "node", "server.js" ]
