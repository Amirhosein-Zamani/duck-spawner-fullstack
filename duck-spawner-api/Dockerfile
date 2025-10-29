FROM node:18-alpine AS builder

WORKDIR /usr/src/app

COPY package.json .
COPY package-lock.json . 

RUN npm install
COPY . .
RUN npm run build

FROM node:18-alpine AS production

WORKDIR /usr/src/app

COPY --from=builder /usr/src/app/node_modules ./node_modules

COPY --from=builder /usr/src/app/dist ./dist
COPY package.json .

CMD ["node", "dist/main.js"]