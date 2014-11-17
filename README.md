# Challenge Week 12 Submission Template

By Nikita Voskoboynik
11/16/14

# Reddit Data Challenges

## Challenge 1

[Imgur](http://i.imgur.com/eND5HgG.jpg)

## Challenge 2

I find it interesting that the field “created_utc” is in a format that can not be read by a human and that one must convert it from PHP to find the actual timestamp of the post. For example, the created_utc field for one post is “1377694742” which means nothing. I had to use the terminal to convert that number to a readable date.

## Challenge 3

One insight I could gain from this dataset is seeing what were the most blogged about topics on Reddit during the course of those two weeks. This would be done using the field “subreddit”. An example of a query to see how many posted had to do with the video game “grand theft auto 5” would look like this: db.reddit.find({"subreddit" : "GrandTheftAutoV"}).count();

## Challenge 4

Pointing to my possible insight in challenge 3, this dataset would tell us the topics that the Reddit Community is talking about as a whole. You could also use keywords to see if the “mood” of the Reddit community was generally happy or sad on a certain day, similar to a tool for Twitter that I have seen.

## Challenge 5

[Link to Code or pasted code]
[Answer]

## Challenge 6

It would mean that the smaller/less popular posts would not be counted and it would mean that we are only analyzing the popular votes and that would give us bias insight.

## Challenge 7

Yes, my conclusions would change because of the bias. For example, for my challenge 3 insight, I would only find out what subreddits are the most popular, not what is most talked about. This is because there could be a lot of posts about unpopular topics, but those would not show up in our sample.

## Challenge 8

It would be bias in the sense that we are not just looking at two of the top 50 subreddits, but two of the top 50 POPULAR and LIKED subreddits. If not considering the scenario mentioned, it is bias because we are looking at the top 50 and ignoring unpopular topics that could have many common commenters.

## Challenge 9

One bias would be because of the time constraint on our data. We have to remember that this is only 2 weeks worth. Another bias would be people commenting things that do not have anything to do with the thread(trolling).

## Challenge 10

To prove that people are trolling, I would simply find a post with a lot of comments and get the body text of all the comments and could then see how many comments are just people trolling.

# Yelp and Weather 

## Challenge 1

db.precipitation.aggregate([{$match:{"date":/20100425.*/}},{$match:{"station.name":"MADISON DANE CO REGIONAL AIRPORT WI US"}},{$group:{_id: null, total_precipitation:{$sum:"$hpcp"}}}])

{ "_id" : null, "total_precipitation" : 62 }

## Challenge 2

db.normal.aggregate([{$match:{"DATE":/20100425.*/}},{$match:{"STATION_NAME":"LAS VEGAS MCCARRAN INTERNATIONAL AIRPORT NV US"}},{$group:{_id: null, avg_windspd:{$avg:"$HLY-WIND-AVGSPD"}}}])

{ "_id" : null, "avg_windspd" : 110.08333333333333 }

## Challenge 3

db.business.aggregate([{$match:{“city”:”Madison”}},{$group:{_id: null, total_reviews:{$sum:”$review_count”}}}])

{ "_id" : null, “total_reviews” : 34410 }

[Imgur](http://i.imgur.com/AqQCays.jpg)

## Challenge 4

db.business.aggregate([{$match:{“city”:”Las Vegas”}},{$group:{_id: null, total_reviews:{$sum:”$review_count”}}}])

{ "_id" : null, “total_reviews” : 577550 }

## Challenge 5

db.business.aggregate([{$match:{“city”:”Phoenix”}},{$group:{_id: null, total_reviews:{$sum:”$review_count”}}}])

{ "_id" : null, “total_reviews” : 200089 }

## Challenge 6 [BONUS]

[Code]
[Answer]



