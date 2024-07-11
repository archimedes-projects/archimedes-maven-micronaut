# Micronaut Maven Kotlin parent

The purpose of this module is to easily add [Micronaut](https://micronaut.io/) support to your **Maven Kotlin projects**.

You can find a **complete example** of how ot use this parent pom in: [micronaut-kotlin-parent-example](https://github.com/archimedes-projects/archimedes-maven-micronaut-examples/tree/main/micronaut-kotlin-parent-example)

If you want to add Micronaut support in your Maven Kotlin project, you need just to set this module as the parent of your project `pom.xml`.

```xml
<?xml version="1.0" encoding="UTF-8"?>
<project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
         xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">
    <modelVersion>4.0.0</modelVersion>

    <parent>
        <groupId>io.archimedesfw.maven.micronaut</groupId>
        <artifactId>micronaut-kotlin-parent</artifactId>
        <version>4.5.0</version>
    </parent>

    <groupId>com.example</groupId>
    <artifactId>my-example</artifactId>
    <version>0.0.1</version>

    ...
```

As you can see in the example, the version of this module corresponds with the Micronaut version that you want to use.


## Integration tests

If you want to run integration tests in your project you just need to activate de [failsafe-maven-plugin](https://maven.apache.org/surefire/maven-failsafe-plugin/) in your project `pom.xml`.

```xml
    ...
    <build>
        <plugins>
            ...
            <plugin>
                <groupId>org.apache.maven.plugins</groupId>
                <artifactId>maven-failsafe-plugin</artifactId>
            </plugin>
            ...
        </plugins>
    </build>
    ...
```
