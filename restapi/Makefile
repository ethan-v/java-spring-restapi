DOCKER_IMAGE_NAME=ethanv/spring-restapi

###======================= SPRING =======================###
dev:
	./gradlew bootRun

# Build app at: ./build/libs/
build-app:
	./gradlew build

verify-app:
	curl http://localhost:8080/hello


###======================= DOCKER =======================###

# Build a docker image with built *.jar file
# docker-build-app-basic:
# 	docker build -t ${DOCKER_IMAGE_NAME} .

# Build a *.jar file on building docker image
docker-build-app:
	export DOCKER_BUILDKIT=1 && docker build -t ${DOCKER_IMAGE_NAME} .

docker-start-app:
	docker run -p 8080:8080 ${DOCKER_IMAGE_NAME}
