FROM node:16 as build
WORKDIR /opt/app
COPY package*.json ./
RUN npm install
COPY . .
ARG PORT=5173
ENV PORT=$PORT
RUN npm run build
CMD ["node", "./index.js"]