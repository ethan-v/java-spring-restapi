DOCKER_IMAGE_NAME=ethanv/spring-restapi

dev:
	./gradlew bootRun

# Build app at: ./build/libs/
build-app:
	./gradlew build

build-docker:
	docker build -t ${DOCKER_IMAGE_NAME} .

start-docker:
	docker run -p 8080:8080 ${DOCKER_IMAGE_NAME}

verify:
	curl http://localhost:8080/hello
