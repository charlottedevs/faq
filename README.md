# faq
frequently asked questions

## How to submit a pull request from your forked repo?

1. After you've forked the repo you want to contribute to, clone the repo locally.


2. Make your changes.


3. When you're done, commit and push the changes you've made to the your forked repo.
_(Note: When you commit, don't forget to include details about the changes you've made in the commit message.)_


4. Visit your forked repo on Github. You should see a banner suggesting you submit a pull request to the original repo. 
If you don't see this, choose the **Pull Request** tab from the ribbon of options at the top of the page and click the 
**New Pull Request** button.
    
    
5. Type in a title and description for your pull request.

   In the description of your pull request be sure to reference the issue you are fixing by simply typing
   `#` followed by the issue number.


6. Click **Create pull request**.

#### Github guides
More detailed instructions on creating a pull request and autolinked references to urls, issues, etc, can be 
found at the following links:

+ https://help.github.com/articles/creating-a-pull-request/ 
+ https://help.github.com/articles/autolinked-references-and-urls/


## How to set up the API?
1. Before you can access the API, you need to install docker toolbox and docker-for-mac (or whichever is appropriate for your machine).

    https://www.docker.com/get-docker

2. Once you have those installed, run the following command in your terminal:
```sh 
touch .env
```
This gives you access to the API's .env file. 

See [here](https://github.com/charlottejuniordevs/api/blob/development/README.md) for instructions on setting up your .env file 
(and keep in mind that this file is required in order to fetch GitHub issues).

3. Finally, you'll need to run the following:
```sh
  docker-compose build
  docker-compose run --rm web bin/setup
  docker-compose up web 
```
This last command starts the server. You'll need to keep this running in a separate tab.

###Sending requests to API via Postman
Postman is a GUI platform designed to make API testing easier. If you don't already have it, you can find it [here](https://www.getpostman.com/).

Once that is up, run the following command in a separate tab to get a JSON web token to use in Postman:
```sh 
docker-compose run --rm web rake token
```
In Postman, you will need to add a header with `Authorization` as the key and `Bearer <your-token-here>` as the value.

You should now be able to send requests to `localhost:3000`.

 