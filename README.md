# microbean-base-specification

The `microbean-base-specification` project specifies the minimal set
of APIs available to any microBean-based application or component.

## Components

The `microbean-base-specification` specifies the following components:

* [Version 1.3 of the Common Annotations for the Java Platform specification][javax-annotations-api].
* [Version 3.0.1-b04 of the Java Expression Language specification][javax-el-api]
* [Version 2.0 of the CDI specification][cdi-api]
* [Version 1 of the `javax.inject` specification][javax-inject]
* [Version 1.2 of the Interceptors specification][javax-interceptor-api]
* [Version 2.0.1.Final of the Bean Validation specification][bean-validation]
* [Version 0.3.0 of the microBean Configuration CDI project][microbean-configuration-cdi]

## Usage

For development, include the following XML stanzas intelligently in your `pom.xml`:

    <dependencyManagement>

      <dependency>
        <groupId>org.microbean</groupId>
        <artifactId>microbean-base-specification</artifactId>
        <version>0.3.0</version>
        <type>pom</type> <!-- Note the type is pom. -->
        <scope>import</scope> <!-- Note the scope is import. -->
      </dependency>
      
      <!-- Other managed dependencies go here. -->
      
    </dependencyManagement>
    
    <dependencies>
    
      <dependency>
        <groupId>org.microbean</groupId>
        <artifactId>microbean-base-specification</artifactId>
        <type>pom</type> <!-- Note the type is pom. -->
        <scope>provided</scope> <!-- Note the type is provided. -->
      </dependency>

      <!-- Other dependencies go here. -->

    </dependencies>

[javax-annotations-api]: https://jcp.org/en/jsr/detail?id=250
[javax-el-api]: https://jcp.org/en/jsr/detail?id=341
[cdi-api]: http://www.cdi-spec.org/download/ 
[javax-inject]: http://javax-inject.github.io/javax-inject/
[javax-interceptor-api]: https://jcp.org/en/jsr/detail?id=318
[bean-validation]: http://beanvalidation.org/2.0/
[microbean-configuration-cdi]: https://microbean.github.io/microbean-configuration-cdi/
