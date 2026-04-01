FROM node:20-alpine3.19 as builder
WORKDIR /build
COPY package*.json .
RUN npm ci && npm cache clean --force
COPY . .
RUN npm run build

FROM nginx:stable-alpine3.17-slim
WORKDIR /app
COPY default.conf /etc/nginx/conf.d/default.conf
COPY --from=builder /build/dist/ .
EXPOSE 80
