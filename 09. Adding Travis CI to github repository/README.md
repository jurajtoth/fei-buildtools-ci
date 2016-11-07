# 9. Adding Travis CI to GitHub repository
1. Travis CI is a hosted continuous integration service that is free for github repositories. We will setup Travis so it will run all tests everytime we push changes to GitHub repository.
2. Click **Sign in with GitHub** to Travis here: [https://travis-ci.org/](https://travis-ci.org/).
3. Click the **+** button in the left panel to add your repository to Travis. Enabled your GitHub repository and click on the name to open the screen where you can see the test executions.
4. Add `.travis.yml` file into the project root with this content: <pre>language: java
	jdk:
      \- oraclejdk8
</pre> This is a initial configuration for Travis.
5. Finally we can push all our changes to GitHub:
	- `git add -A`
	- `git commit -m "Project migrated to Maven"`
	- `git push`
6. This push will automatically trigger Travis build which you can check on Travis website.

Next exercise: [10. Configuring Travis to send mail notification](https://github.com/jurajtoth/fei-buildtools-ci/tree/master/10.%20Configuring%20Travis%20to%20send%20mail%20notification)