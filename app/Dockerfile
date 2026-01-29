
FROM node:20-alpine 


WORKDIR /app


COPY app/package*.json ./


RUN npm ci --only=production && npm cache clean --force


COPY app .

EXPOSE 3000
USER node

# Start the application
CMD ["node", "app.js"]
