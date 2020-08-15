# Skeleton node.js app
The purpose of this app is quickly test out container services that you may be
interested in testing such as spinning up containers on EC2 instances, Elastic
Container Service using Fargate, Elastic Kubernetes Service etc.

### Build & Run
If you want to build locally:
```
docker build -t neelypatel/pet-superstore-api .
```
or you can pull the latest image:
```
docker pull neelypatel/pet-superstore-api
```
To run it:
```
docker run -d --name pet-superstore-api -p 3000:3000 neelypatel/pet-superstore-api
```
Go to `localhost:3000` to see the message. You can also do a healthcheck at `localhost:3000/healthcheck`.

### Docker Compose
Start the app and the database:
```
docker-compose up -d --build
```
shut it all down:
```
docker-compose down
```

### Upcoming features
* instructions and config for deploying to various AWS services and GCP services
* kubernetes related instructions and config
* automated testing and CI environment

### dockerhub page
https://hub.docker.com/r/neelypatel/pet-superstore-api
