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
        <version>2.5.4</version>
    </parent>

    <groupId>com.example</groupId>
    <artifactId>my-example</artifactId>
    <version>0.0.1</version>

    ...
```

As you can see in the example the version of this module correspond with the Micronaut version that you want to use.

This module allow you to mix Kotlin and Java source files in the same Maven module, the firs one in `src/main/kotlin` and the other in `src/main/java` (and the equivalent `src/test/kotlin` and `src/test/java` for the test sources).

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

## Lombok

This module preconfigure the [Lombok](https://projectlombok.org/) annotation processor to be compatible with micronaut, so if you want to use **Lombok in your Java sources** you just need to activate the library dependency in you project `pom.xml`.

```xml
    ...
    <dependencies>
        ...
        <dependency>
            <groupId>org.projectlombok</groupId>
            <artifactId>lombok</artifactId>
        </dependency>
        ...
    </dependencies>
    ...
```

## Typical Micronaut plugins

There are several Maven plugins that are usually used with Micronaut. If you want to use some already configured plugins you just need to activate it in your project `pom.xml`.

For example to generate an auto-executable jar you can use:

```xml
    <properties>
        ...
        <exec.mainClass>com.example.Application</exec.mainClass>
        ...
    </properties>

    <build>
        <plugins>
            ...
            <plugin>
                <groupId>org.codehaus.mojo</groupId>
                <artifactId>exec-maven-plugin</artifactId>
            </plugin>
            ...
        </plugins>
    </build>
    ...
```
