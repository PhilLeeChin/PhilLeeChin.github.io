---
layout: post
title:      "Rising Challenges"
date:       2020-04-20 17:04:57 +0000
permalink:  rising_challenges
---


As this new epidemic cripples the economy, working, taking care of family, and school has proven to be alot more of a challenge than before. With finishing my degree in Computer Science hoping that this is my last semester, it has proven to be very challenging with the distance learning. Math class is alot more difficult because of how it is being taught. My CS-281 course - Data Structures - is challenging but it is bareable, learning sql with postgres, and eventually in MySQL, Cassandra, MongoDB, and Spark. More challenges rising doing my best to stay head strong to stay on task.

It was fun working on my CLI project, was neverous but my reviewer Howard made me feel comfortable, and I was able to complete aadding in a new method that checked for beers with strong alcohol levels:
```
def self.strong_beers
    all.select {|s_beer| s_beer.abv > 5}
end
```

After that I also worked on adding a method that checks for all beers that has low alcohol levels:
```
def self.weak_beers
    all.select {|w_beers| w_beers.abv < 5}
end
```

Thanks to Howard I learnt how to use the select method instead of an if statement to do itteration. Now as the next module starts and the focus is SQL with ruby objects, starting off it is pretty straight forward as it is working with basic SQL commands to create a table, insert data, and to query those data to get results. I have fallen behind as I have not completed last weeks work as of yet, and I also have this week set to do as well.

My peer-partner Peter is great to work with and talk to as we both understand each other, and able to help with completing ideas. I hope to finish all by the end of this week so that I am not totally left behind.
