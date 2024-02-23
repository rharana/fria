# Build environment
FROM node:16-alpine as build
WORKDIR /frontend
COPY package.json package-lock.json ./
RUN npm install
COPY . ./
RUN npm run build

# Production environment
FROM nginx:stable-alpine
COPY --from=build /frontend/build /usr/share/nginx/html
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
