FROM eclipse-temurin:19-jdk-alpine
VOLUME /tmp
WORKDIR /workspace/app

ARG BUILD_JAR_DIR=build/libs
ARG JAR_FILE_PLAIN=${BUILD_JAR_DIR}/*SNAPSHOT-plain.jar
ARG JAR_FILE=${BUILD_JAR_DIR}/*SNAPSHOT.jar

COPY ${JAR_FILE_PLAIN} app-plain.jar
COPY ${JAR_FILE} app.jar

RUN pwd
RUN ls -la

ENTRYPOINT ["sh", "-c", "java ${JAVA_OPTS} -jar /workspace/app/app.jar ${0} ${@}"]
