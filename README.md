# drone.io_docker-compose
docker-compose file for drone.io version 1


```
docker run \
  --volume=/var/run/docker.sock:/var/run/docker.sock \
  --env=DRONE_DATABASE_DRIVER=${DRONE_DATABASE_DRIVER} \
  --env=DRONE_DATABASE_DATASOURCE=${DRONE_DATABASE_DATASOURCE} \
  --env=DRONE_GITHUB_SERVER=https://github.com \
  --env=DRONE_GITHUB_CLIENT_ID=${DRONE_GITHUB_CLIENT_ID} \
  --env=DRONE_GITHUB_CLIENT_SECRET=${DRONE_GITHUB_CLIENT_SECRET} \
  --env=DRONE_RUNNER_CAPACITY=2 \
  --env=DRONE_SERVER_HOST=${DRONE_SERVER_HOST} \
  --env=DRONE_SERVER_PROTO=http \
  --env-file .env \
  --publish=80:80 \
  --publish=443:443 \
  --name=drone \
  --add-host postgres.whyservices.net:10.0.0.154 \
  drone/drone:1.0.0-rc.1

  ```
