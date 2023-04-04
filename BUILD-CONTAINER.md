# alertmanager-dockerfile
build alertmanager container image with only dockerfile

## Example build process
```
docker build --no-cache --tag alertmanager:0.24.0-paxos .
docker tag alertmanager:0.24.0-paxos 769032674102.dkr.ecr.us-east-1.amazonaws.com/sre/alertmanager:0.24.0-paxos
docker push 769032674102.dkr.ecr.us-east-1.amazonaws.com/sre/alertmanager:0.24.0-paxos
```
