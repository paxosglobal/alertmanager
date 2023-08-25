# alertmanager-dockerfile
build alertmanager container image with only dockerfile

## Example build process
```sh
__branch="$(git branch --show-current)"
__tag="${__branch#release-}"
docker build --no-cache --file="Dockerfile.build-image" \
  --build-arg "AM_BRANCH=${__branch}" \
  --tag "alertmanager:${__tag}" \
  .
docker tag alertmanager:${__tag} 769032674102.dkr.ecr.us-east-1.amazonaws.com/sre/alertmanager:${__tag}
docker push 769032674102.dkr.ecr.us-east-1.amazonaws.com/sre/alertmanager:${__tag}
```




## See Jenkins job:
* https://github.com/paxosglobal/sre/blob/master/Jenkinsfile#L52
* https://jenkins.private.mgmt.mgmtnonprod.net/job/sre/job/test-dockerbuild/job/master/

...then PR to change AM_BRANCH in
  [sre.git//docker/alertmanager/Dockerfile](https://github.com/paxosglobal/sre/blob/master/docker/alertmanager/Dockerfile)





