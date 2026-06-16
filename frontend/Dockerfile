FROM ubuntu:24.04
WORKDIR /usr/src/app

ENV REACT_APP_BACKEND_URL=http://localhost:8080
COPY . .
RUN apt-get update && apt-get install -y curl
RUN curl -sL https://deb.nodesource.com/setup_16.x | bash && apt-get update
RUN apt-get install -y nodejs && npm install && npm run build && npm install -g serve

ENTRYPOINT ["serve", "-sl", "5001", "build"]


