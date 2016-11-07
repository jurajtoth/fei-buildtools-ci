# 11. Creating a single archive from your application
1. Running the application is difficult, as you have to include the libraries on the classpath. We will create a single application archive, which can be launched more easily.
2. To do this, add a Maven plugin with the following XML snippet placed right after the </dependencies> element:
<pre>&lt;build&gt;
        &lt;plugins&gt;
                &lt;plugin&gt;
                        &lt;groupId&gt;org.apache.maven.plugins&lt;/groupId&gt;
                        &lt;artifactId&gt;maven-assembly-plugin&lt;/artifactId&gt;
                        &lt;version&gt;2.6&lt;/version&gt;
                        &lt;configuration&gt;
                                &lt;descriptorRefs&gt;
                                        &lt;descriptorRef&gt;jar-with-dependencies&lt;/descriptorRef&gt;
                                &lt;/descriptorRefs&gt;
                                &lt;archive&gt;
                                        &lt;manifest&gt;
                                                &lt;mainClass&gt;sk.fei.ci.MovieList&lt;/mainClass&gt;
                                        &lt;/manifest&gt;
                                &lt;/archive&gt;
                        &lt;/configuration&gt;
                        &lt;executions&gt;
                                &lt;execution&gt;
                                        &lt;id&gt;assemble-all&lt;/id&gt;
                                        &lt;phase&gt;package&lt;/phase&gt;
                                        &lt;goals&gt;
                                                &lt;goal&gt;single&lt;/goal&gt;
                                        &lt;/goals&gt;
                                &lt;/execution&gt;
                        &lt;/executions&gt;
                &lt;/plugin&gt;
        &lt;/plugins&gt;
&lt;/build&gt;</pre>
3. Go to commandline, to the folder with the project and execute `mvn clean package`
4. After finished, Maven built us a single .jar file, which contains all the classes including the dependencies. 
Launch the application by executing `java -jar target/movielist-maven-0.0.1-SNAPSHOT-jar-with-dependencies.jar` 
5. Point your browser to [http://localhost:4567/hello](http://localhost:4567/hello) to test the application
6. Stop the application with CTRL + C in the commandline
7. Commit the application changes with `commit -a`
8. Push the latest changes to Github wiht `git push origin master`

Last exercise: [12. Deploying the application to Heroku](https://github.com/jurajtoth/fei-buildtools-ci/tree/master/12.%20Deploying%20the%20application%20to%20Heroku)