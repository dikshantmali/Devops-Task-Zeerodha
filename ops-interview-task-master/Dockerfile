FROM golang:1.21-alpine
RUN apk update && apk add curl make
ENV DEMO_APP_ADDR=0.0.0.0:3000
ENV DEMO_REDIS_ADDR=redis:6379
WORKDIR /app
COPY . ./
RUN make build
EXPOSE 8080
CMD [ "./demo.bin" ]
