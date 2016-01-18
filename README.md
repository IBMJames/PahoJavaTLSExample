# PahoJavaTLSExample
An example Maven Project that uses Eclipe Paho Java client to publish a message over a TLS connection.

## Build and Run

 * To build: ```mvn package```
 * Then to run it: ```java -cp target/my-app-1.0-SNAPSHOT-jar-with-dependencies.jar org.eclipse.paho.App```

## Change Dependency Version
The ```pom.xml``` file currently references the Paho SNAPSHOT repository.
To use the main release, change the repository url to: ```https://repo.eclipse.org/content/repositories/paho-releases/``` and change the dependency version to: ```1.0.2```.


## Add a new certificate for a different server
To add a certificat for a different server, add it to the ```src/main/resources``` directory
then change the line defining ```certificateName``` in [this](src/main/java/org/eclipse/paho/App.java) source file to the new certificate name:

```String certificateName = "iot.eclipse.org.crt";```
##
