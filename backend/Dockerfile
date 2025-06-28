FROM node:20-alpine
WORKDIR /opt/backend
COPY *.js .
COPY package.json .
RUN npm install
ENV DB_HOST="mysql"
CMD ["node", "index.js"]