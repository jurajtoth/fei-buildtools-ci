# 5. Converting project to Maven structure
1. Using Maven means having a project structured according to Maven's common directory layout
	- you can check it here: [https://maven.apache.org/guides/introduction/introduction-to-the-standard-directory-layout.html](https://maven.apache.org/guides/introduction/introduction-to-the-standard-directory-layout.html)
2. All application sources are located in `src/main/java` folder. Create this folder and place your `MovieList.java` source file there. You final folder structure should be `src/main/java/sk/fei/ci/MovieList.java`
3. All application test sources are located in `src/test/java` folder. Create this folder and place your `MovieListTest.java` source file there. You final folder structure should be `src/test/java/sk/fei/ci/MovieListTest.java`
4. You can delete `run.bat` and `run-test.bat` files. We won't be using those to build or test our project anymore.