# Heroku Setup

### Heroku

Heroku is a free hosting site similar to AWS, Azure, etc... I like it as it's super easy to deploy to and test out things in the real world. Best of all though is it's completely **FREE** 👻  

First things first we're going to need you to get setup on the heroku side of things:  
* Go to [Heroku](https://signup.heroku.com/‎) and sign up
* Navigate to the [Heroku CLI tools](https://devcenter.heroku.com/articles/heroku-cli)
  - If you have [Homebrew](https://brew.sh/) installed then I'd suggest using that for the easiest way. Just run the following from your terminal:

`$ brew tap heroku/brew && brew install heroku`

Once it's installed, close you terminal and reopen it then type:

`$ heroku -v`

If it's worked then it should give you a version number  

Now you'll just need to login with:

`$ heroku login -i`

If you miss the '**-i**' off the end then it'll take you to the site to login, which is fine. I just prefer to stay in the terminal wherever possible

***
### Make an app

Or better yet, use one of the ones you have already on your machine. I'd say anything in Javascript that you can run on **localhost** is a suitable candidate