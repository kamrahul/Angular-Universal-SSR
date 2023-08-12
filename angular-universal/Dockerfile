# Stage 1: Build Angular App
FROM node:14 as build-stage

WORKDIR /app

# Copy package.json and package-lock.json
COPY package*.json ./





RUN ls
# Install dependencies
RUN npm install

# Copy the rest of the application code
COPY . .

# Build the Angular app for production
RUN npm run build:ssr

# Stage 2: Serve Angular App with SSR
FROM node:14

WORKDIR /app

# Copy the built Angular Universal artifacts from the previous stage
COPY --from=build-stage /app/dist /app/dist
#COPY --from=build-stage /app/server.js /app/server.js
COPY --from=build-stage /app/package.json /app/package.json

# Install production dependencies
RUN npm install --only=production

# Expose the port on which the server will run
EXPOSE 4000

# Start the server
## Start the application
CMD ["node", "dist/angular-universal/server/main.js"]
