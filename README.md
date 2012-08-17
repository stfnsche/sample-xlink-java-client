How to configure & build
==========================
- Install & Configure Java JDK 1.6 or higher

- Install & Configure Maven 3.0 or higher

- Clone and Build (mvn clean install) the [OpenEngSB](https://github.com/openengsb/openengsb-framework) with XLink and the Domains 'SQLCreate' and 'OOSoureCode' 

- Clone and Build (mvn clean install) the [java-loom Bridge](https://github.com/openengsb/loom-java.git)

- Build (mvn clean install) this project

- You find the program in the directory 'target', its 'org.openengsb.xlink.xlinkjavaclient-[version]-jar-with-dependencies.jar'

- To run the program, got to 'target/classes' and copy the files 'application.properties' 
and 'log4j.properties' into the same directory as your .jar

- Configure the program arguments in 'application.properties'
	1) Change Username, Password and Context if necessary.
	2) If the OpenEngSB Server is not running on your local machine, the 'xlink.baseUrl' has to be changed as well.
	3) Set the 'working.dir' to a local directory.
	4) Copy the 'creates.sql' to this directory.

- Start the OpenEngSB server and make sure that the JMS-Port bundle is installed

- Start the Java-Client

Structure of accepted SQL files
==========================
The Program filters SQL CreateStatements in this abstract syntax

A Statement is of the structure

CREATE TABLE <TABLENAME>
(
 <fieldName> <dataType> <listOfConstraints>,
);

Make sure that the opening and closing bracket have no leading or trailing spaces.
Every fieldDefintion must be written in it�s own row.

Accepted Constraints are
 PRIMARY KEY
 NOT NULL
 REFERENCES <tableName>(<fieldName>)


Implemented Functionality
==========================
- TBW

Not yet Implemented Functionality
==========================
- 'Local Switch' functionality
- Adding of 'Create Statements'