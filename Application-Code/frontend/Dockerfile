
# Stage 1 - Build
FROM node:14 AS builder

WORKDIR /usr/src/app

COPY package*.json ./

RUN npm install

COPY . .


# Stage 2 - Distroless Runtime
FROM gcr.io/distroless/nodejs14

WORKDIR /usr/src/app

COPY --from=builder /usr/src/app .

CMD ["npm", "start"]
