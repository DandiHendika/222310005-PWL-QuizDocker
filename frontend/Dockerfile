# frontend/Dockerfile

# --- Tahap 1: Build Aplikasi React ---
FROM node:18-alpine as build

WORKDIR /app
COPY package.json ./
RUN npm install
COPY . .
RUN npm run build

# --- Tahap 2: Sajikan dengan Nginx ---
FROM nginx:stable-alpine
COPY --from=build /app/dist /usr/share/nginx/html
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]