# Getting Started

### Build Code
* ./gradlew clean build
docker run --rm -v "$PWD":/home/gradle/project -w /home/gradle/project gradle:7.3.1-jdk11 gradle clean build

### Run Jar
* Local:      ./gradlew bootRun 
* Pipeline:   nohup bash gradlew bootRun &

docker run --rm -p 8082:8082 -v "$PWD":/home/gradle/project -w /home/gradle/project gradle:7.3.1-jdk11 gradle bootRun

### Testing Application
* curl -X GET 'http://localhost:8082/rest/mscovid/test?msg=testing'


