FROM openjdk:17-jdk-slim AS builder
WORKDIR /app
COPY ./*.java .
RUN javac ChatServer.java

FROM openjdk:17-jdk-slim
WORKDIR /app
COPY --from=builder /app .

ENTRYPOINT [ "java","ChatServer.java"]