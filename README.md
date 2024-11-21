# UserService
Steps to run Course Master Service

Run mysql via docker using following command: 
**docker run -p 3330:3306 --name userservicecontainer -e MYSQL_PASSWORD=Bits@2024 -e MYSQL_USER=sa -e MYSQL_ROOT_PASSWORD=Bits@2024 -e MYSQL_DATABASE=userservicedb  mysql:8.3.0 -d **

First run might take time as image might be getting downloaded.
Build the service using mvn clean install. First run might take time depending on the network connection and available mirrors.
Run the service either through IntelliJ Idea or through commandline by navigating to the folder in which pom.xml is present: mvn spring-boot:run. The service will run on port 2020.
To access database from commandline/terminal run the command: 
**docker exec -it userservicecontainer bash **
to access the container followed by 
**mysql -u sa userservicedb -p **
which will prompt to enter password.
