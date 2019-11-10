# CodeBeamer widget development bootstrap project

This project is meant to be the starting point for widget development in the codeBeamer ALM system.

## Requirements

Building the API client SDK requires:
1. Java 1.8+
2. Gradle
3. Locally installed codeBeamer instance

## Installation

To include the proper codeBeamer API, open the /build.gradle file and modify the codeBeamerInstallDir definition to the root path of your codeBeamer instance:

```groovy
def codeBeamerInstallDir = '{codeBeamer installation directory}'
```
## Getting started

After the [installation](#installation) you will be able to build a basic widget:

```shell script
./gradlew clean build
```

To deploy the widget you can use the following command:

```shell script
./gradlew deploy
```

It will copy the newly build jar into local codeBeamer installation.

To enable the newly deployed widget you'll need to restart the codeBeamer instance:

```shell script
./gradlew stopCB
```

```shell script
./gradlew startCB
```

Now you should be able to see your newly created widget:
![Hello World widget](img/helloworld.png?raw=true)