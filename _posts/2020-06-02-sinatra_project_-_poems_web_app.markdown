---
layout: post
title:      "Sinatra Project - Poem's Web App"
date:       2020-06-02 21:01:03 +0000
permalink:  sinatra_project_-_poems_web_app
---


Accomplishing a degree and overcoming another Project.

At the beginning of project week I was so far behind, in labs, and with trying to finish off my college degree. A week and a half into project week I was able to complete my last two class at college socring an A- and a B to finish off my associates degree. It feels so full filling to be done and walking away with a degree in the area I love. Thanks to my pair partner Peter Bedrosian, my cohort lead Z and Katie. They was there for me through this time pushing me to go the mile, to achieve, motivating guiding me through.

Now to talk more about the project, when I met with my pair partner Peter and with his guidance, and example of his web app I knew what I wanted to make my project off. I was creating a website to host the poems that I have been writing, with activerecords and Sinatra I am able to do some methods that I was not able to implement as of yet in my website. I have learnt through this project how to get a submission button and login page setup. After my assessment I will use this project to further establish my website. 

With this web app, users can create their own poems, edit it, and even delete it. Through a few methods I am able to display information stored in the database.

this method displays the user name as the author of the poem:
`<h2> Author: <%=Helpers.name(session)%></h2>`

While these two methods shows when the user created the poem, and when/if they have updated it:
`<h3 style="font-family: 'Lobster Two', cursive;"> Date Created: <%=@poem.created_at.strftime("%m-%d-%Y at %H:%M %p")%></h3>`

`<h3 style="font-family: 'Lobster Two', cursive;"> Date Updated: <%=@poem.updated_at.strftime("%m-%d-%Y at %H:%M %p")%></h3>`

Now one thing I came across while working on the project is that if a user enters their username without the first letter capitalized it will stay that way, unless the enter the name with a capital first letter. Through some research I found that I can use the .capitalize ruby method to change the lower case first letter to a uppercase:
```
def self.name(session)
  self.current_user(session).username.capitalize
end
```

The routes did give me some trouble to pull off, but another collegue Daniel Sasser, whom helped me test and also figure out that the redirect block is used with double quotes " " and not the single ' '. It was fun working on this project, and just like before another hurdle overcome as I continue to press on through climbing the Mountains of code.
