# 6. Runtime dependencies
1. Our sample application is dependent on a small library called **Spark**.
	- this library is located in the `lib\spark-core-2.5.jar` file in the project
	- **Spark** library is also dependent on other libraries and all are located in the `lib` folder.
	- you can already see how many files we need to manually manage in the `lib` folder and we are only using 1 library. Maven will help us with this :)
2. Delete the `lib` folder with all the libraries.
3. Create a new file named `pom.xml` in the root of the project folder
4. Copy this content to the file <pre>&lt;project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd"&gt;
		&lt;modelVersion&gt;4.0.0&lt;/modelVersion&gt;
		&lt;groupId&gt;sk.fei.ci&lt;/groupId&gt;
		&lt;artifactId&gt;movielist-maven&lt;/artifactId&gt;
		&lt;version&gt;0.0.1-SNAPSHOT&lt;/version&gt;
		&lt;properties&gt;
			&lt;maven.compiler.target&gt;1.8&lt;/maven.compiler.target&gt;
			&lt;maven.compiler.source&gt;1.8&lt;/maven.compiler.source&gt;
			&lt;project.build.sourceEncoding&gt;UTF-8&lt;/project.build.sourceEncoding&gt;
		&lt;/properties&gt;
		&lt;dependencies&gt;
		&lt;/dependencies&gt;
&lt;/project&gt;</pre>
5. Go to maven repository and check the Spark library here: [https://mvnrepository.com/artifact/com.sparkjava/spark-core/2.5](https://mvnrepository.com/artifact/com.sparkjava/spark-core/2.5)
6. Add this library as our project's depedency. Paste this code <pre>&lt;dependency&gt;
    	&lt;groupId&gt;com.sparkjava&lt;/groupId&gt;
    	&lt;artifactId&gt;spark-core&lt;/artifactId&gt;
   		&lt;version&gt;2.5&lt;/version&gt;
&lt;/dependency&gt;</pre> inside the `<dependencies>` element in pom.xml.
7. Compile the application using `mvn compile` command from command-line. You will see all dependencies deleted in step 2 downloaded automatically by maven.
8. Check the compiled application in the `target` folder.