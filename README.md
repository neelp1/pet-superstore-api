# pet-superstore-api
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

### Docker Compose (easiest)
Start the app:
```
docker-compose up -d --build
```
Information on how to start the app that this superstore calls can be found:
https://github.com/neelp1/pets-app
pets-app will connect to the pet-superstore-api network if started with docker compose.

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
