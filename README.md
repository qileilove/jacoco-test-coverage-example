# jacoco-test-coverage-example
```
mvn install
```

## start jacoco agent
java -javaagent:src/main/resources/lib/jacocoagent.jar=address=*,port=36320,destfile=jacoco-it.exec,output=tcpserver -jar target/jacoco-code-coverage-example-0.0.1-SNAPSHOT.jar

## curl services
curl -X GET http://localhost:8080/test/9
curl -X GET http://localhost:8080/test/50

## dump jacoco runtime data
java -jar src/main/resources/lib/jacococli.jar dump --address localhost --port 36320 --destfile target/jacoco-it.exec

## export jacoco report
java -jar src/main/resources/lib/jacococli.jar report target/jacoco-it.exec --classfiles target/classes/com --sourcefiles src/main/java/ --html target/jacoco-report

https://dzone.com/articles/code-coverage-report-generator-for-java-projects-a
