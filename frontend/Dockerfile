# ------------------- Stage 1: Build Stage ------------------------------
FROM node:21 AS frontend-builder

# Set working directory
WORKDIR /app

# Copy package.json and install dependencies
COPY package*.json ./
RUN npm install

# Copy rest of the code and build
COPY . .
RUN npm run build

# ------------------- Stage 2: Serve with Nginx -------------------------
FROM nginx:alpine

# Copy custom nginx config
COPY nginx.conf /etc/nginx/conf.d/default.conf

# Copy build output from frontend-builder
COPY --from=frontend-builder /app/dist /usr/share/nginx/html

# Expose port 80
EXPOSE 80

# Start nginx
CMD ["nginx", "-g", "daemon off;"]
