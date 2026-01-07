FROM node:18-alpine
WORKDIR /app
COPY package*.json ./
RUN npm ci --omit=dev --silent && npm cache clean --force
COPY src ./src
RUN chown -R node:node /app
USER node
CMD ["node", "src/index.js"]
