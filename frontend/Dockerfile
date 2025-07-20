# 1. Build Stage: schlankes Node-Alpine zum Installieren & Bauen
FROM node:18-alpine AS builder
WORKDIR /app

# Installiert und kopiert Abhängigkeiten und das bauen das Frontend
COPY . .
RUN npm install
RUN npm run build

# 2. Serve Stage: nginx-alpine serviert die statischen Dateien
FROM nginx:alpine
COPY --from=builder /app/dist /usr/share/nginx/html

EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
