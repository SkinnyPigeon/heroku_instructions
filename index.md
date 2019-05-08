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

Once you've picked one, doesn't have to be a super fancy one as this time is just for practice. Avoid any that reference databases at this stage. We can cover that another time 😵

Might be worth making a copy of the file or jumping onto another Git Branch if you're comfortable doing that. Anyhoo once you're happy to proceed you'll need to do the following:  
* Go into the **server.js** file and change the **app.listen()** function to:

```javascript
app.listen(process.env.PORT || 3000, function() {...
```
* Next you'll need to create a thing called a **Procfile**
  - This needs to be created in the root of the app's directory so go navigate to the app's folder in terminal and type:

`$ touch Procfile`  
Notice there's no extension on it, it's just **Procfile**

* Open your newly created **Procfile** in your favourite text editor (cough, cough, [Visual Studio Code](https://code.visualstudio.com/download)), and put the following:

```javascript
web: node server.js
```

That's it! We're ready to get this online 🤩

***
### 
