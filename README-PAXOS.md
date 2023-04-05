# alertmanager-dockerfile
build alertmanager container image with only dockerfile

## Example build process
```
docker build --no-cache --tag alertmanager:0.24.0-paxos .
docker tag alertmanager:0.24.0-paxos 769032674102.dkr.ecr.us-east-1.amazonaws.com/sre/alertmanager:0.24.0-paxos
docker push 769032674102.dkr.ecr.us-east-1.amazonaws.com/sre/alertmanager:0.24.0-paxos
```




## See Jenkins job:
* https://github.com/paxosglobal/sre/blob/master/Jenkinsfile#L52
* https://jenkins.private.mgmt.mgmtnonprod.net/job/sre/job/test-dockerbuild/job/master/

...then PR to change AM_BRANCH in
  [sre.git//docker/alertmanager/Dockerfile](https://github.com/paxosglobal/sre/blob/master/docker/alertmanager/Dockerfile)





