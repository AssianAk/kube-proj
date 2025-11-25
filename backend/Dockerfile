FROM node:18 as build
WORKDIR /app
COPY package.json package-lock.json ./
RUN  npm install
RUN npm install -g pm2
COPY . .
EXPOSE 3000
EXPOSE 80
CMD [ "pm2-runtime","index.js","--name","backendapi" ]
