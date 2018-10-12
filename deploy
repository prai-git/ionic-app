# file-service

## 1. Prerequisite - 
    Install Maven latest version
    Install Java latest version


## 2. Evnironment Specific changes (DEV/Testing/Staging..etc)

### 2.1 database changes in /file-service/src/main/resources/application.properties

#### Connection url for the database "PRINTER"
    spring.datasource.url = jdbc:mysql://localhost/PRINTER?useUnicode=true&characterEncoding=UTF-8

#### Username and password
    spring.datasource.username = root
    spring.datasource.password = Pass1234!

### 2.2 port changes in /file-service/src/main/resources/application.properties
    server.port=9080

### 2.3 Logging changes in file /file-service/src/main/resources/log4j2.xml
    $ Current Path: /home/developer/logs/fileservice.log

## 3. Deploying

### 3.1 Creating an Executable Jar:
Executable jars (target/file-service-0.0.1-SNAPSHOT.jar) are archives containing your compiled classes along with all of the jar dependencies that your code needs to run.
#### Command 
    $ mvn clean package

If you look in the target directory, you should see (target/file-service-0.0.1-SNAPSHOT.jar). The file should be around 50 MB in size. 

### 3.2 Copy this Jar to remote server:
    $ scp target/file-service-0.0.1-SNAPSHOT.jar <remote/local server path>

## 4. Execute(Run). 

### 4.1 run with default property file that is defined in class path. (/file-service/src/main/resources/application.properties)
    $ java -jar file-service-0.0.1-SNAPSHOT.jar

OR

### 4.2 Configure the property file from class path in resource folder: (/file-service/src/main/resources/QA/application.properties)
    $ java -jar file-service-0.0.1-SNAPSHOT.jar --spring.config.location=classpath:/QA/application.properties

OR
### 4.3 Configure the multiple properties file from class path in resource folder, next property file will override the previous property file:

    $ java -jar file-service-0.0.1-SNAPSHOT.jar --spring.config.location=classpath:/application.properties, classpath:/QA/application.properties
    
OR 

### 4.4 Configure the property file from file location: 
    $ java -jar file-service-0.0.1-SNAPSHOT.jar --spring.config.location=file:<./scm/../src/main/resources/QA/application.properties>
    
