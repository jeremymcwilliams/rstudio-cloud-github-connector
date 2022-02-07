# rstudio-cloud-github-connector
Shortcut function for establishing a connection between rstudio.cloud and github, because setting your token over and over is a drag.


In rstudio.cloud, when working on a project based upon a github respository, one has to intially set environment variables for github user & email, and then periodically set the user's github token. The steps here would be:

* Get a user token (https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token). 
* Create a new project in rstudio.cloud, based on a github repository (make sure the repository has a .gitignore file). 
* Copy the contents of github.sample.R into a file called "github.R".  
* Edit the function near the top to include github username, email, and token.
* Edit .gitignore file to include github.R (this will prevent your token from ending up in the repository).
* Run the `githubConnect()` function whenever you load rstudio.cloud for the affected project.
