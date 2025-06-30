FROM node:20.18.3-alpine3.21
RUN addgroup -S rk && adduser -S rk -G rk
RUN mkdir /opt/backend
RUN chown -R rk:rk /opt/backend
WORKDIR /opt/backend
COPY *.js .
COPY package.json .
RUN npm install
ENV DB_HOST="mysql"
USER rk
CMD ["node", "index.js"]