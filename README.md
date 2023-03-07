# docker-test
Test docker for rxinui-teaching/01-introduction-ci-cd

Build a docker image from a Dockerfile
```sh
docker build -t yolo-apache:latest .
```

Create and run a container from a docker image
```sh
docker run --rm --name yolo-1 -p 8080:80 yolo-apache:latest
```

Test the apache server with curl and get HTTP status
```sh
curl -s -I localhost:8080 | head -1
```