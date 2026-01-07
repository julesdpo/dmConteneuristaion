FROM node:18-alpine
WORKDIR /app
COPY package*.json ./
RUN npm ci --silent && npm cache clean --force
COPY . .
RUN chown -R node:node /app
USER node
CMD ["npm", "run", "dev", "--", "--host", "0.0.0.0", "--strictPort", "--port", "4173"]
