### Perfecto + Maven + Testng + Java Sample Project: ![CircleCI status](https://circleci.com/gh/PerfectoMobileSA/MavenCircleCISample.svg?style=shield "CircleCI status")

This sample project is designed to get you up and running within few simple steps.

Begin with installing the dependencies below, and continue with the Getting Started procedure below.

### Dependencies
There are several prerequisite dependencies you should install on your machine prior to starting to work with this project:

* [Java 8](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)

* An IDE to write your tests on - [Eclipse](http://www.eclipse.org/downloads/packages/eclipse-ide-java-developers/marsr) or [IntelliJ](https://www.jetbrains.com/idea/download/#)

* [Maven](https://maven.apache.org/)

Eclipse users should also install:

1. [Maven Plugin](http://marketplace.eclipse.org/content/m2e-connector-maven-dependency-plugin)

2. [TestNG Plugin](http://testng.org/doc/download.html)

IntelliJ IDEA users should also install:

1. [Maven Plugin for IDEA](https://plugins.jetbrains.com/plugin/1166)

TestNG Plugin is built-in in the IntelliJ IDEA, from version 7 onwards.
 
#### Optional Installations
* For source control management, you can install [git](https://git-scm.com/downloads).

## Downloading the Sample Project

* Clone this repository.

* After downloading and unzipping the project to your computer, open it from your IDE by choosing the folder containing the pom.xml 

# Getting Started

* Configure the name of your Perfecto cloud as a system variable by passing your cloud name as a -DcloudName=<<cloud name>> from Maven system property while running the install goal of Maven or simply hardcode your cloud name in the script.

* Configure your security token from Maven by passing the -DsecurityToken=<<token>> system property while running the install goal of Maven or simply hardcode it.

* Run pom.xml with the below maven goals & properties

		clean
		install
		-DcloudName=${cloudName}
		-DsecurityToken=${securityToken}

* Maven will take care of kick starting the parallel execution of different examples inside perfecto package in parallel.

### Circle CI Integration:
* This project contains a .yml file under .circleci / config.yml which will help CircleCI’s webhooks to listen for git updates. 
* It will also print the suite level report at the end of execution.
* It is configured to schedule everyday at 12:00am UTC. 
* The current build status of CircleCI in github will be showcased in readme.md file. Here's [how](https://circleci.com/docs/2.0/status-badges/) to set it up.
