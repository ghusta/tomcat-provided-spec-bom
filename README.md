# Maven BOM for Tomcat 9.0 provided dependencies

A Maven BOM to simplify dependencies management in your webapp.

## Provided specifications

- Servlet 4.0 - [JSR 369](https://jcp.org/en/jsr/detail?id=369)
- JSP 2.4 (TBD) - [JSR 245](http://jcp.org/en/jsr/detail?id=245)
- EL 3.1 (TBD) - [JSR 245](http://jcp.org/en/jsr/detail?id=245)
- WebSocket 1.2 (TBD) - [JSR 356](https://jcp.org/en/jsr/detail?id=356)
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
                <version>9.0</version>
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
