FROM maven:3.5-jdk-8-alpine AS builder
RUN mkdir /worker
COPY . /worker/
WORKDIR /worker

RUN mvn dependency:resolve
RUN mvn package

FROM openjdk:8-jre-alpine

RUN mkdir /worker
COPY --from=builder /worker/target/ /worker/target/
WORKDIR /worker
CMD java -jar target/worker-jar-with-dependencies.jar
