# quarkus-config-yaml-live-reload project

Small project to showcase [a pull request on the main quarkus.io repository](https://github.com/quarkusio/quarkus/pull/6386)

# Usage

## The problem

Start the project in dev mode with `./mvnw clean compile quarkus:dev` then make a request in another terminal with to confirm
 everything started properly:
```
curl http://localhost:8080/greeting
```

Make any change to the file `src/main/resources/application.yaml`, save it, make another request... No hot reload :(

## The solution

- Clone [the forked quarkus project](https://github.com/devauxbr/quarkus/tree/feature/application-yaml-hot-reload), checkout branch `feature/application-yaml-hot-reload` and build with `./mvnw clean install`
- In `pom.xml` of this current project comment line 19 and uncomment line 20 (this will use the locally built version of quarkus)
- retry the previous paragraph steps -> hot reload works, hurray !
