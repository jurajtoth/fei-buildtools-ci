# 8. Packaging application
1. Our basic maven project setup is finished.
2. Packaging our application is very easy. Run `mvn package` command.
3. This command will also run previous phases (`compile` and `test` phase).
  - you can read more about maven's lifecycle here: https://maven.apache.org/guides/introduction/introduction-to-the-lifecycle.html
4. Check your packaged **jar** application in the generated `target` folder.

Next exercise: [9. Adding Travis CI to GitHub repository](https://github.com/jurajtoth/fei-buildtools-ci/tree/master/09.%20Adding%20Travis%20CI%20to%20github%20repository)