# Maven BOM for Tomcat 8.5 provided dependencies

A Maven BOM to simplify dependencies management in your webapp.

## Provided specifications

- Servlet 3.1 - [JSR 340](https://jcp.org/en/jsr/detail?id=340)
- JSP 2.3 - [JSR 245](http://jcp.org/en/jsr/detail?id=245)
- EL 3.0 - [JSR 341](http://jcp.org/en/jsr/detail?id=341)
- WebSocket 1.1 - [JSR 356](https://jcp.org/en/jsr/detail?id=356)
- JASPIC 1.1 - [JSR 196](https://jcp.org/en/jsr/detail?id=196)

The versions used are summarized here :
[Apache Tomcat Versions](http://tomcat.apache.org/whichversion.html)

## Usage

The BOM must be imported as scope "import" with the "pom" type, in the dependencyManagement section. 

    <dependencyManagement>
        <dependencies>
            <dependency>
                <groupId>fr.husta.tomcat</groupId>
                <artifactId>tomcat-provided-spec-bom</artifactId>
                <version>8.5</version>
                <type>pom</type>
                <scope>import</scope>
            </dependency>
        </dependencies>
    </dependencyManagement>

Then, simply import the needed dependency without specifying the version.

    <dependencies>
        <dependency>
            <groupId>javax.servlet</groupId>
            <artifactId>javax.servlet-api</artifactId>
            <scope>provided</scope>
        </dependency>
    </dependencies>

## Maven documentation

About the _"bill of materials"_ (BOM) : [Introduction to the Dependency Mechanism](https://maven.apache.org/guides/introduction/introduction-to-dependency-mechanism.html#Importing_Dependencies)

Another example of BOM usage with Spring Framework : http://platform.spring.io/platform/#quick-start
