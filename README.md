# Micronaut Maven base parent

The purpose of this module is to easily add [Micronaut](https://micronaut.io/) support to your Maven projects. 

[Since Micronaut 2.0 this module is based on the official Micronaut pom-parent](https://docs.micronaut.io/2.0.0/guide/index.html#whatsNew), 
and this module defines some more Maven 
properties with typical values or package versions. Just simply are defaults values that you can override in your 
project `pom.xml` to change the default behaviour.

In this module you can find the configuration of some typical Maven plugins that are used with Micronaut. 
Please refer to the `pom.xml` of this module to see these configurations.
 
This is a Maven base module just to define some common defaults, so is preferred that you don not use it directly 
and instead in your project you should use one of:
 
 - [micronaut-java-parent](https://github.com/autentia/micronaut-java-parent)
 - [micronaut-kotlin-parent](https://github.com/autentia/micronaut-kotlin-parent)
