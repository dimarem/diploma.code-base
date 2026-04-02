ARG NODEJS_VERSION=20-alpine3.19

FROM node:${NODEJS_VERSION} as builder
WORKDIR /build
COPY package*.json .
RUN npm ci && npm cache clean --force
COPY . .
RUN npm run build

FROM nginx:stable-alpine3.19
WORKDIR /app
COPY default.conf /etc/nginx/conf.d/default.conf
COPY --from=builder /build/dist/ .
USER nginx
EXPOSE 80
