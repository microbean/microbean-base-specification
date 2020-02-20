# microBean™ Base Specification

The `microbean-base-specification` project specifies the minimal set
of APIs available to any microBean™-based application or component.

## Components

The `microbean-base-specification` specifies the following components:

* [Version 1.3.5 of the Jakarta Annotations specification](https://jakarta.ee/specifications/annotations/1.3/)
* [Version 3.0.3 of the Jakarta Expression Language specification](https://jakarta.ee/specifications/expression-language/3.0/)
* [Version 2.0.2 of the Jakarta Contexts and Dependency Injection specification](https://jakarta.ee/specifications/cdi/2.0/)
* [Version 1.0 of the Jakarta Dependency Injection specification](https://jakarta.ee/specifications/dependency-injection/1.0/)
* [Version 1.2.5 of the Jakarta Interceptors specification](https://jakarta.ee/specifications/interceptors/1.2/)
* [Version 2.0.2 of the Jakarta Bean Validation specification](https://jakarta.ee/specifications/bean-validation/2.0/)
* [Version 0.0.4 of the microBean™ Settings project](https://microbean.github.io/microbean-settings/)

## Usage

For development, include the following XML stanzas **intelligently**
in your `pom.xml`:

    <dependencyManagement>

      <dependency>
        <groupId>org.microbean</groupId>
        <artifactId>microbean-base-specification</artifactId>
        <version>0.6.1</version>
        <type>pom</type> <!-- Note the type is pom. -->
        <scope>import</scope> <!-- Note the scope is import. -->
      </dependency>
      
      <!-- Other managed dependencies go here. -->
      
    </dependencyManagement>
    
    <dependencies>
    
      <dependency>
        <groupId>org.microbean</groupId>
        <artifactId>microbean-base-specification</artifactId>
        <!-- Note no version is provided -->
        <type>pom</type> <!-- Note the type is pom. -->
        <scope>provided</scope> <!-- Note the scope is provided. -->
      </dependency>

      <!-- Other dependencies go here. -->

    </dependencies>
