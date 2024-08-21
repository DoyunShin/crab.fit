FROM node:18-alpine

WORKDIR /app

ENV NEXT_TELEMETRY_DISABLED 1

COPY package.json yarn.lock ./
RUN apk add --no-cache curl && yarn install

COPY . .
# RUN yarn build

EXPOSE 3000

CMD ["sh", "-c", "yarn build && yarn start"]