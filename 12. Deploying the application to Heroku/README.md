# 12. Deploying the application to Heroku
1. You will need to register Heroku account [https://signup.heroku.com/login](https://signup.heroku.com/login) and login to the account
2. After login go to the dashboard, showing your applications [https://dashboard.heroku.com/apps](https://dashboard.heroku.com/apps)
3. Select Create New App and fill in the following details:
	1. App Name: based on the folder name of your application
	2. Runtime Selection: Europe (so your application is not running in USA)
4. In the Deploy tab on Heroku select Deployment method: Github / Connect to GitHub
5. Use the search boxes to find your repository and connect it
6. Select Enable Automatic Deploys
7. In the Manual Deploy part select master branch and click Deploy Branch
8. Heroku still does not know what your application is. To be able to discover this, create file `Procfile` in the root directory of your application
9. Paste the following content into the file:
<pre>web: java -jar target/movielist-maven-0.0.1-SNAPSHOT-jar-with-dependencies.jar $PORT</pre>
This will tell Heroku, that you have a web application and the command to launch it 
10. Commit and push your changes
11. Go to Heroku application configuration page and select Activity tab. On this tab you can view the build progress, wait some time until it is finished
12. Once done, you can go to Resources tab. You should see there the content of the Procfile. Click the edit button on the right, move the trigger to turn on the Dynos on Heroku and select Confirm
13. And then you can access your application by clicking on the Open app button in Heroku and navigating to `/hello` URL.