# Welcome to Kal-Config Store

- This repository containt properties/yml files in order to provide remote configuration for my Microservices

- This repository is served by [kal-config-server](https://github.com/Kalystee/kal-config-server) and a microservice (Python, Java, C#) can be
connected to kal-config-server

## Security

:warning: Do not add secrets in __clear text__
Use the encrypt endpoint first with a curl, http client, postman...

```
### Encrypt value from json
POST {{uri}}/encrypt
Content-Type: text/plain

{{value_to_be_encrypted}}

> {% client.global.set("encrypted_value", response.body.toString()); %}
```
- You will get an encrypted value, use this value in your yml file, __do not forget to add the prefix {cipher} 
    > "{cipher}00ae9f52989c0aa6345c1fd87ab81caef51db2b796007b01522601b6a6e1c1a8"
    - :warning: Do not use double quotes intp "*.properties" files
## Consuming for various clients
### Java - Spring Boot

- Add this dependency to your pom.xml
```xml
<dependency>
    <groupId>org.springframework.cloud</groupId>
    <artifactId>spring-cloud-starter-config</artifactId>
</dependency>
```