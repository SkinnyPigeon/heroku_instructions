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
### Create the webapp  

Head over to your apps section on the [Heroku website](https://dashboard.heroku.com/apps), click on the '**New**' button, and select '**Create new app**' from the drop down menu. This'll bring you to a page that let's you pick a name for your app and where it'll get hosted

As hopefully you've noticed, this site has a crazy name. That's what happens when you leave it blank. For development I tend to let it generate names like this since otherwise I might be depriving someone of a name they really want, and I've already taken it for some banal purpose. For you proudest creations, go crazy and name it whatever you want

Usually it's a good idea to change the region in the '**Choose a region**' dropdown to **Europe**

When you're ready click on '**Create app**'

You will now see how simple it is to deploy to Heroku. They have super clear instructions which I will steal wholecloth to look like I know what I'm doing:  

* Hopefully you are still in your code's root folder and hopefully you have used **Git** on it throughout your development of it 😋
* If not then we'll:  

`$ git init`  

* In the case of this site I wrote the following, obviously you'll just be copying straight from the Heroku instructions but for illustrative purposes:

`$ heroku git:remote -a obscure-beach-50298`

* Now we're getting close:  

`$ git add .`  
`$ git commit -m "about to push to heroku!"`  
`$ git push heroku master`

If everything has worked *(and I genuinely will be surprised if my instructions haven't missed out something important)* then you should see some nonsense filling your terminal. If it's been successful then the last few lines will mention things like '**Compressing...**' and '**Launching**' and, almost finally, '**Verifying deploy... done**'  

Now we jump back to the page in Heroku that contained the deployment instructions. Scroll back to the top and click on '**Open app**' in the top right 🤞. Moment of truth...   

Wait a few seconds before panicking. These are free servers and can take a wee while to spin up but if we're lucky you should see you site in all its glory

If it hasn't worked then just let me know and we'll get it sorted as deploying is super fun and let's start making your imprint online. I have a tonne of silly things out there thanks to Heroku. I've also done some cool things with it too so please do give this a try

Thanks,   
Euan
