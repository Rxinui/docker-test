# docker-test
Test docker for rxinui-teaching/01-introduction-ci-cd

Build a docker image from a Dockerfile
```sh
docker build -t yolo-apache:latest .
```

Create and run a container from a docker image
```sh
docker run -d --rm --name yolo-1 -p 8080:80 yolo-apache:latest
```
**NOTE**: on GitHub Actions `-d` flag is important otherwise, the step is blocked and cannot move forward.

Test the apache server with curl and get HTTP status
```sh
curl -s -I localhost:8080 | head -1
```