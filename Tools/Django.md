# Django

Before you go too deep into the Django world, make sure you check out the general python stuff we have over at the [Python](https://github.com/ArcticWarriors/snobot2015/wiki/Django) page


## Django Description
Django is a tool for creating websites with python.  It has a lot of cool features and forces you to work in an MVC design pattern.  Their instructions are here https://docs.djangoproject.com/en/1.8/howto/windows/
Go to https://www.djangoproject.com/download/ and download the latest release tar file
Hopefully you have something that can extract tar files, if not get 7-ZIP
Extract it onto your desktop (or wherever, you can delete it later)
Open a command window in the folder you just extracted
Neat trick, if you open the folder in explorer, you can go to the address bar, type cmd, and hit enter, and it will open the prompt in that folder
Type into the prompt “setup.py install” (without quotes)
If it says something like it can’t find python or it doesn’t know how to run it, go to the “Fixing Path” section, then come back here and try again

You should now (maybe) have everything you need installed.

NOTE: You might see the following errors which can be ignored...

    Extracting Django-1.9.1-py2.7.egg to c:\python27\lib\site-packages
      File "c:\python27\lib\site-packages\Django-1.9.1-py2.7.egg\django\conf\app_template\apps.py", line 1
        {{ unicode_literals }}from django.apps import AppConfig
                             ^
    SyntaxError: invalid syntax

      File "c:\python27\lib\site-packages\Django-1.9.1-py2.7.egg\django\conf\app_template\models.py", line 1
        {{ unicode_literals }}from django.db import models
                             ^
    SyntaxError: invalid syntax

## Running the example
I recommend going through the Django tutorials to learn about what is going on in the background before diving headfirst into the ocean.  But if you feel like it, I created an exampleand pushed it to GitHub.  The example is loosly based on the tutorial with different table names and a different app name.  If you get to the admin section, I set up an account.  Username: snobot_sw, password: team174rocks.  Note: this is also the password (maybe some caps in there) for our SW team’s email address arcticwarriors174.software@gmail.com 

### Quick Setup Guide
Make sure everything is installed first
Open a command prompt in the DjangoExample folder (wherever your local github stuff goes).  Recall the command prompt trick from before
If you have GitHub installed, open it and sync () all the changes and then click on top right hand corner. From there select ‘Open in Explorer’ and the DjangoExample folder should be located there.
If GitHub says you have uncommitted changes and you must commit them or discard them then right-click around the area that says changes and select ‘Discard all changes’. After that you should be able to sync. 
Run the following command (no quotes): “python manage.py runserver”.  Theoretically you should see something like this to indicate that it worked
If there is an error, or something other than what is above shows up then open eclipse and go to: DjangoExample>DjangoExample>settings.py and place a # in front of ‘junctionTable’ to comment it out.

In your web browser, navigate to http://127.0.0.1:8000/firstApp/ and behold my semi-purposly bad app
Using Python and Django
You guys have very little experience with python, but it is a pretty easy language to pick up.  There are good tutorials on the website https://docs.python.org/2/tutorial/, and stackoverflow and other online things have plenty of resources for getting started and answering questions.  

The big thing that will look odd to you at first is there are no braces.  Python uses spaces to to figure out “what would be in a brace”, so the code can look cleaner .  Python also uses Duck Typing, so variable MY_VAR might be an integer one line, then a string the next, and a class the next.  There are other syntactic differences that you will pick up over, I will make plenty of examples for you to look at.  Python has a tremendous amount of syntactic sugar to play with, it is a lot of fun

Django has a steeper learning curve, especially since you don’t know python.  I will be setting up an example project shortly, and we can add info to here when we run into problems or questions or whatever.

## Web Design Preface
You go to websites every day, but probably don't know too much about how they work.  When you go to a website like amazon or netflix a few things happen.  

When you make a request to their server (by going to netflix.com) it will do a lot of processing on the server side.  It might look up your browser cookies and say, oh this is PJ, I’ll automatically log him in and show him movies he recently watched and stuff we recommend.  To look up what movies it should display, it will look at some sort of database and look at my viewing habits.  It then will take all of that information and turn it into some HTML code that my browser can interpret and turn into something to display to me.  

Most websites also have some client side code which makes it easier to navigate the website.  Websites that do stuff like photo viewing have buttons that let you navigate through the pictures without having to talk to the server again.  Some websites have countdowns which are handled through a small piece of javascript.

Another thing the client side code does is make the website look pretty.  It will say “hey, render the background as red, the text as white, have all of the links be white and then turn blue when I hover over them,” etc.  This is primarily done through a CSS file which specifies how to display your HTML code.

Now let’s put this in terms of a scouting website.  Someone might want to navigate to a page showing them the stats for a team.  We can look up all of that teams matches from our database on the server side, and use that to create an HTML page.  We can use some client side code to create table that can be sorted, or to create some graphs that we can change without having to reload the page.  While all of this is going on, someone with a much better eye for design than I have will have created a CSS template that will specify what color the page is and how the big the font is.

To sum up, we will be doing three things.  Creating server side code using Python and Django to render an HTML5 website, using client side code like javascript or ajax or something I have never heard of to make the website more usable, and using CSS3 to create something that is actually nice to look at.

