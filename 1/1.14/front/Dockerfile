FROM node:16.16.0-alpine3.16


EXPOSE 5000

WORKDIR /usr/src/app

RUN npm install -g serve

COPY ./material-applications/example-frontend/package* .

RUN npm install

COPY ./material-applications/example-frontend .

RUN REACT_APP_BACKEND_URL="http://localhost:8080" npm run build

CMD ["serve", "-s", "-l", "5000", "build"]