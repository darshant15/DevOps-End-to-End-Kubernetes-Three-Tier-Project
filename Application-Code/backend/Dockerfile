# Stage 1 - Dependencies
FROM node:22-bookworm-slim AS builder

WORKDIR /usr/src/app

COPY package*.json ./

RUN npm ci --omit=dev

COPY . .


# Stage 2 - Distroless Runtime
FROM gcr.io/distroless/nodejs22-debian12

WORKDIR /usr/src/app

COPY --from=builder /usr/src/app /usr/src/app

EXPOSE 3000

CMD ["index.js"]
