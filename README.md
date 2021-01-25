```
FROM golang:1.8-onbuild

Generating local image :
sudo -s
docker build -t golang-first .
docker images
docker run -d -p 80:80 golang-first
Go to http://localhost/
docker kill
docker ps -a
docker rm f c83
docker stop golang-test
docker rmi golang-test -f

Pushing to docker hub :

docker tag golang-first saiashish9/golang-first:latest
docker images
docker push saiashish9/golang-first
docker rmi -f golang-first 7e7 saiashish9/golang-first
docker search  saiashish9/golang-first

Pulling from docker hub:

<!-- docker pull saiashish9/golang-first -->
docker run -d -p 80:80 saiashish9/golang-first
docker tag saiashish9/golang-first golang-first
```