# 10. Configuring Travis to send mail notification
1. Add email notification setting to **.travis.yml** configuration. Fill your email address. <pre>language: java
jdk:
      \- oraclejdk8
notifications:
      email:
        \- email@address.com</pre>
2. Push this change to GitHub same as in previous exercise.
3. Push will trigger Travis build and you will receive an email after the build is finished.

Next exercise: [11. Creating a single archive from your application](https://github.com/jurajtoth/fei-buildtools-ci/tree/master/11.%20Creating%20a%20single%20archive%20from%20your%20application)
