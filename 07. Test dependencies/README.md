# 7. Test dependencies
1. Similar to runtime dependency **Spark**, our project is using a library called **JUnit** for running tests.
2. Check JUnit library in maven repository: [https://mvnrepository.com/artifact/junit/junit/4.12](https://mvnrepository.com/artifact/junit/junit/4.12)
3. Similar to **Spark** library, add also **JUnit** library to our project but with **test scope** <pre>&lt;dependency&gt;
   		&lt;groupId&gt;junit&lt;/groupId&gt;
    	&lt;artifactId&gt;junit&lt;/artifactId&gt;
    	&lt;version&gt;4.12&lt;/version&gt;
		&lt;scope&gt;test&lt;/scope&gt;
&lt;/dependency&gt;</pre>
	- you can read more about maven depedency scopes here: [https://maven.apache.org/guides/introduction/introduction-to-dependency-mechanism.html#Dependency_Scope](https://maven.apache.org/guides/introduction/introduction-to-dependency-mechanism.html#Dependency_Scope)
4. run tests using `mvn test` command from command-line. You will see maven downloading **JUnit** library automatically. After that you should see all tests pass successfully.
	