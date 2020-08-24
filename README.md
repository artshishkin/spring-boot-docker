#Spring Boot and Docker

Source code in this repo is to support my on line course for Docker and Spring Boot. 

You can learn more about my course [here](http://courses.springframework.guru).

##  Section 5 - DevOps - Automating Building of Docker Images

### Tasks
1.  Adding Fabric8 Maven Plugin (43)
2.  Enabling connect to remote docker daemon
    -  `https://nickjanetakis.com/blog/docker-tip-73-connecting-to-a-remote-docker-daemon`
3.  Creating Docker Image in Fabric 8 (44) 
    -  `mvn clean package docker:build`
4.  Pushing to Dockerhub (45)
    -  create dockerhub account
    -  add server to maven `settings.xml`:
    -  encrypt password by using `mvn --encrypt-password`
```xml
<server>
    <id>docker.io</id>
    <username>artarkatesoft</username>
    <password>{your_encrypted_password}</password>
</server>
```
    -  run `mvn clean package docker:build docker:push`
