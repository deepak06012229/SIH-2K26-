FROM node:18-alpine

WORKDIR /app

COPY package.json package-lock.json* ./

RUN npm install

COPY . .

# Build the frontend for production
RUN npm run build

# Start the Vite preview server or a simple node server
# Or we can just use npm run preview, or expose 3000 as per docker-compose.yml
CMD ["npm", "run", "dev", "--", "--host", "0.0.0.0", "--port", "3000"]
