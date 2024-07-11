[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg?style=flat)](https://www.apache.org/licenses/LICENSE-2.0)
[![Maven Central](https://img.shields.io/maven-central/v/io.archimedesfw.maven.micronaut/micronaut-base-parent.svg?label=Maven%20Central)](https://search.maven.org/search?q=io.archimedesfw.maven.micronaut)
[![Java CI](https://github.com/archimedes-projects/archimedes-maven-micronaut/workflows/Java%20CI/badge.svg)](https://github.com/archimedes-projects/archimedes-maven-micronaut/actions)

# Micronaut Maven base parent

The purpose of this module is to easily add [Micronaut](https://micronaut.io/) support to your Maven projects. 

[Since Micronaut 2.0 this module is based on the official Micronaut pom-parent](https://docs.micronaut.io/2.0.0/guide/index.html#whatsNew), 
and this module defines some more Maven 
properties with typical values or package versions. Just simply are defaults values that you can override in your 
project `pom.xml` to change the default behavior.

In this module you can find the configuration of some typical Maven plugins that are used with Micronaut. 
Please refer to the `pom.xml` of this module to see these configurations.
 
This is a Maven base module just to define some common defaults, so is preferred that you do not use it directly 
and instead in your project you should use one of:
 
 - [micronaut-java-parent](https://github.com/archimedes-projects/archimedes-maven-micronaut/tree/main/micronaut-java-parent) - only Java project
 - [micronaut-kotlin-parent](https://github.com/archimedes-projects/archimedes-maven-micronaut/tree/main/micronaut-kotlin-parent) - only Kotlin project
 - [micronaut-kotlin-java-parent](https://github.com/archimedes-projects/archimedes-maven-micronaut/tree/main/micronaut-kotlin-parent/micronaut-kotlin-java-parent) - project that mix Java and Kotlin sources


# JDK 21

Because JDK 21 is the actual LTS version, since version 4.5.0 of this module, JDK 21 is used by default.

If you want to use another JDK version you can define it in your module `pom.xml` using the properties:

```xml
    <properties>
        <jdk.version>17</jdk.version>
        <release.version>17</release.version>
    </properties>
```

# Micronaut Maven plugin

Since versión 4.5.0 of this module, the official Micronaut Maven plugin is used.
This simplifies the Maven configuration and allows using in your projects some invaluable features such as:

 - [Integration with Micronaut Test Resources](https://micronaut-projects.github.io/micronaut-maven-plugin/latest/examples/test-resources.html) to automatically create needed Docker containers during integration tests,
 - [Package the application as `docker` or `native-image` or...](https://micronaut-projects.github.io/micronaut-maven-plugin/latest/examples/package.html) with zero additional configuration,
 - [Run the application in development mode](https://micronaut-projects.github.io/micronaut-maven-plugin/latest/examples/run.html) with `mvn mn:run`,
 - ...
