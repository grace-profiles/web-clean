# Grace Web Profile

A profile for creating Grace web applications, support `Tomcat`, `Jetty`, `Undertow` embedded server, support database such as `h2`, `MySQL`, `MariaDB`, `PostgreSQL`, and with more flexible and optional **Features**.

## Grace Stack

- Grace **2022.0.0**
- Gradle **7.6.3**
- Spring Framework **5.3.25**
- Spring Boot **2.7.9**
- Micronaut **3.8.6**

## Usage

Grace `web-clean` profile based on `base` profile, unlike `web` profile, except support `Tomcat`, also support `Jetty`, `Undertow` embedded server, support database such as `h2`, `MySQL`, `MariaDB`, `PostgreSQL`, with more optional dependencies and features, such as `actuator`, `scaffolding`, `async`, `events`, `cache`, `json-views`, you can add later if needed.

### Build Profile

```
git clone https://github.com/grace-profiles/web-clean.git
cd web-clean
./gradlew publishToMavenLocal
```

### Create App

#### Use Tomcat with default features

```
grails create-app --profile web-clean org.grails.demo.web-clean-demo
cd web-clean-demo
grails run-app
```

#### Use Jetty

```
grails create-app --profile web-clean --features actuator,console,hibernate5,i18n,interceptors,logging,rest,scaffolding,testing,validation,jetty org.grails.demo.web-clean-demo
cd web-clean-demo
grails run-app
```

#### Use Undertow

```
grails create-app --profile web-clean --features actuator,console,hibernate5,i18n,interceptors,logging,rest,scaffolding,testing,validation,undertow org.grails.demo.web-clean-demo
cd web-clean-demo
grails run-app
```

## What's New

### 2022.0.0

* Update Grace 2022.0.0
* More improvements and bug fixes
* Provider embedded servlet server:
  - Tomcat
  - Jetty
  - Undertow
* Support databases:
  - h2
  - mariadb
  - mysql
  - postgresql
  - mongodb
  - neo4j
* Support individual and optional features:
  - actuator
  - **asset-pipeline**
  - *async*
  - *cache*
  - console
  - *database-migration*
  - *events*
  - *geb2*
  - **gsp**
  - hibernate5
  - i18n
  - interceptors
  - *json-views*
  - logging
  - *markup-views*
  - rest
  - *rx-mongodb*
  - scaffolding
  - testing
  - validation

## Links

- [Grace Framework](https://graceframework.org)
- [Grace](https://github.com/graceframework)
- [Grace Web Bootstrap Profile](https://github.com/grace-profiles/web-bootstrap)
