docker_container_name=base

docker build -t msct/$docker_container_name $docker_container_name

docker push msct/$docker_container_name