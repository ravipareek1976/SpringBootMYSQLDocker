# Example Dokcer MySQL , Spring Boot Crud

 reference location : https://www.youtube.com/watch?v=U2GCM0GBzNI
 
##Commands
1) docker pull mysql  // pull the image of docker
2) docker run -p 3307:3306 --name  mysqldb -e MYSQL_ROOT_PASSWORD=root -e MYSQL_DATABASE=test mysql:8.0.13 // run the mysql and set password root, with environment variable
3) docker network create spring-network // create netowrk names spring-network

