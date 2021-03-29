# HELLO WORLD SPARK APP
for this project, I am using
- Maven Build Tool
- Visual Studio Code

## Instructions for creating a hello world program using the Spark Framework (sparkjava.com).

- Create a folder called "first_spark_app"
- Navigate to the "first_spark_app" directory from the terminal.

Inside the first_spark_app directory:
- Create a new directory called "my_app" and navigate to that directory from the terminal.
- Inside the my_app directory, create a pom.xml file.

- Go to the Java Spark documentation at http://sparkjava.com/tutorials/maven-setup and copy their example of a pom.xml file into your own. 

- Edit the groupid to say "my_app" and groupid to say "com.leehaney" (add your own name instead of mine). Your artifactid is the root folder of your project. Your root
folder is what contains your pom.xml file and src folder. It is where you will compile
and run your project.

- Be sure to include the following dependency to your pom.xml dependencies:

        <dependency>
            <groupId>org.slf4j</groupId>
            <artifactId>slf4j-jdk14</artifactId>
            <version>1.7.30</version>
        </dependency>


- Add the following directories and java file with these commands (from the my_app directory):
$ mkdir src; mkdir src/main; mkdir src/main/java; mkdir src/main/java/com; mkdir src/main/java/com/leehaney; touch src/main/java/com/leehaney/App.java

- Run the following command (from the same folder as the pom.xml file)
- $ <b>mvn compile</b>
- $ <b>mvn clean install</b> &nbsp;&nbsp;&nbsp;---> (If needed) The clean command will delete all previously compiled Java.class files and resources.
- $ <b>mvn exec:java -Dexec.mainClass="com.leehaney.App"</b>


In the browser, type in: localhost:4567/hello
You should see "Hello World" on the screen

# How to use this project
- Download this project from the terminal with $<b>git clone https://github.com/leeb2828/first_spark_app </b>
- Inside the my_app directory (contains pom.xml file), run the following commands:
- $ <b>mvn compile</b> &nbsp;&nbsp;&nbsp; ---> a new "target" folder will be created.
- $ <b>mvn exec:java -Dexec.mainClass="com.leehaney.App"</b>
- In the browser, type in <br>localhost:4567/hello <br>
You should see "Hello World" on the screen


If you see the following error message:

SLF4J: Failed to load class "org.slf4j.impl.StaticLoggerBinder".<br>
SLF4J: Defaulting to no-operation (NOP) logger implementation<br>
SLF4J: See http://www.slf4j.org/codes.html#StaticLoggerBinder for further details.<br>

It means you need to include an slf4j logging implementation in your maven dependencies
For example, add the following to your pom.xml dependencies:

        <dependency>
            <groupId>org.slf4j</groupId>
            <artifactId>slf4j-jdk14</artifactId>
            <version>1.7.30</version>
        </dependency>
