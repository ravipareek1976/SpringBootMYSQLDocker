# Example Dokcer MySQL , Spring Boot Crud

 reference location : https://www.youtube.com/watch?v=U2GCM0GBzNI
 
##Commands
1) docker pull mysql  // pull the image of docker
2) docker run -p 3307:3306 --name  mysqldb -e MYSQL_ROOT_PASSWORD=root -e MYSQL_DATABASE=test mysql:8.0.13 // run the mysql and set password root, with environment variable
3) docker network create spring-network // create netowrk names spring-network
4) crete SpringBoot Jar runas-->maven install
5) docker build -t springboot-mysql-docker .   // create the docker image of Application
6) docker images  // verify image created
7) docker network connect spring-network mysqldb   // bind DB to Docker network spring-network
8) docker inspect spring-network // verify binding
9) -DMYSQL_HOST=localhost  -DMYSQL_PORT=3307  -DMYSQL_USER=root  -DMYSQL_PASSWORD=root    // these are passed in IDE Eclipse as parameters   refer below location//https://www.devinline.com/2015/10/program-and-vm-arguments-in-java.html#:~:text=Pass%20program%20and%20VM%20arguments%20in%20eclipse%3A%2D&text=Right%20click%20on%20project%20%2D%3E%20Go,12%20added%20separated%20by%20spaces).
10) docker run -p 9090:8080 --name springboot-mysql-docker --net spring-network -e MYSQL_HOST=mysqldb -e MYSQL_USER=root -e MYSQL_PSSWORD=root -e MYSQL_PORT=3306 springboot-mysql-docker // not this command should be in online, no newline character
11) now hit the URL http://localhost:9090/student/insert post the payload in postman
    {
    "name": "spring boot aaaa",
    "age": 23
    }
   

