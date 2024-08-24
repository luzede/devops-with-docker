FROM golang:1.16.15-alpine3.15

EXPOSE 8080

WORKDIR /usr/src/app

COPY ./material-applications/example-backend .

RUN go build

ENV PORT=8080
ENV REQUEST_ORIGIN=https://example.com
# ENV REDIS_HOST=localhost
# ENV POSTGRES_HOST=localhost
# ENV POSTGRES_USER=postgres
# ENV POSTGRES_PASSWORD=postgres
# ENV POSTGRES_DATABASE=postgres

CMD ["./server"]