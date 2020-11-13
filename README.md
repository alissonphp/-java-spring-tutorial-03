# Java Tutorials: #03 Building a RESTful Web Service with Spring Boot Actuator and start with Integration Tests
#### Main goal:

- Use Actuator
- Create a controller to return hello world message
- Check actuator management routes
- Write initial integration tests

#### References:

- [spring guide](https://spring.io/guides/gs/actuator-service/)

#### Results:
get default message
```shell script
> curl http://localhost:9000/hello-world
{"id":1,"content":"Hello, Anyone!"}
```
get message from route param
```shell script
> curl http://localhost:9000/hello-world\?name\=Alisson
{"id":3,"content":"Hello, Alisson!"}
```

get actuator management health check
```shell script
> curl http://localhost:9001/actuator/health
{"status":"UP","components":{"diskSpace":{"status":"UP","details":{"total":226242326528,"free":185449164800,"threshold":10485760,"exists":true}},"ping":{"status":"UP"}}}
```

test results
