# salt-docker

# salt-master
cd salt-master-docker
docker build -t salt-master:1.0.0 .
docker run -d --net=host salt-master:1.0.0

# salt-minion
cd salt-minion-docker
docker build -t salt-minion:1.0.0 .
docker run -d --net=host salt-minion:1.0.0
