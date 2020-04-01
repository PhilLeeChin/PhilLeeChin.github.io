---
layout: post
title:      "Beer Info CLI project"
date:       2020-04-01 16:23:06 +0000
permalink:  beer_info_cli_project
---


First time working with an API to create a App

No challenge never comes easy, but the harder the challenge once completed makes us feel even better about ourselves. When project week kicked in, it was in high gear to complete it with 2 weeks. Having adequate time to first think of what you want your app to do, then to find the appropriate API to return the data needed, and finally to create the app. I came accross a few API's that I wanted to use, because I wanted to build a API that users would be able to learn information about highly favoured games before buying them. My first API was great as it was returning the data that I needed, but it held me at a stand still because I was unable to figure out the neccessary params to input to get the right data. This was the IGDB API, I also looked at RAWG but it too was not giving me back the data I wanted. 

After talkin to my cohort lead Z Drake, she advised me to find a different API, and after a short search I came accross https://api.punkapi.com. This API has a database of beers and unique details for them. This API was much more easier to use, to call the data, to return it, to search through it, and to pick out what specific details I need to return to the user. Since my API stores the information for each beer in an array of hashes, I was able to call from this url:

https://api.punkapi.com/v2/beers/?page=1&per_page=15

I also specified to have the API return one page of information, with 15 beers to the page. My first issue was how to get to pull the information from the API, I watched a couple videos and in each found that they used the .map method that returns a new array with the modified elements. For my API I was able to use the ".each do" method and pipe to a variable for storing the data.

```
response.each do |beer|
    new_beer = Beer.new(beer['name'], beer['tagline'], beer['first_brewed'], beer['description'], beer['abv'])
end
```

With this method in place these variables would be called in to the CLI class to return the details to the user after selecting a beer from the numbered list.

```
def display_details
    puts "**************************************************"
    puts "--------------------------------------------------"
    puts "Label: " + @beer.name
    puts "Tagline: " + @beer.tagline
    puts "Month and Year 1st Brewed: " + @beer.brew_date
    puts "Info: " + @beer.description
    puts "Alcohol level: " + @beer.abv.to_s + "%"
    puts "--------------------------------------------------"
    puts "**************************************************"
end
```

Now the question of where is all this information passing in from, the Beer class, with the objects created there I was able to pass the data from the API into each object of the class, as the class initialize it creates an instance variable for each detail. I added a call variable which was an array, using the shovel operator "<<" to store the information into the class variable to make the app easier to work with the data. Pulling the information, itterating through it, and returning the details for each beer.

It was fun working with this API and was over joyed that I was now complete with my app. For the final touches I customized it so that it was more user friendly:

```
def welcome_message
	puts "**************************************************"
	puts "**************************************************"
	puts "*****      Welcome to my Beer info app       *****"
	sleep(1)
	puts "*****   Find out unique information about    *****"
	puts "*****               Each Beer                *****"
	puts "**************************************************"
	puts "**************************************************"
end
```

I also added "system('clear') after the user selection in order to clear the terminal screen so that it does not become clustered. It was fun working on this project, and just like before another hurdle overcome as I continue to press on through climbing the Mountains of code.
