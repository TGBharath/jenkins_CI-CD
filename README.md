# jenkins_CI-CD

to install jenkins on docker


docker container run -d \
  -p 8080:8080 \
  --env JENKINS_OPTS="--prefix=/jenkins" \
  -v jenkins:/var/jenkins_home \
  jenkins/jenkins:lts

