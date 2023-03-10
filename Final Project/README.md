# NLP_340 Project

## Background

In the sport of soccer, every club has goals and expectations. These goals are set to keep the fans happy and keep the club profitable. When a manager can't keep with these goals, or sometimes more importantly the expectations of the fans, the manager is the first to take the blame and likely to get sacked. It is not uncommon for managers to get sacked (fired) in the sport of soccer. This season in the English Premier League, 8 of the starting 20 managers have been sacked, and South Hampton has gone through 2 managers already.

## Goal

As a long time avid enjoyer of soccer, I want to study sentiment analysis of comments from soccer clubs social media accounts because I want to see if I can predict when a manager is likely to be sacked. Since fans have a large impact on profit, through shirt sales and in game support, they have a role in making change for the club. I'm curious to see if negative sentiment in comments can drive this change. I also want to see how sentiment changes between comments after a one-off loss and a chain of bad form.

## FAQ

**Where will the data be extracted from?**

The data will be scraped from social media comments. Using Twarc2 (if twitter is still available for scraping) I can pull replies to tweets from a variety of clubs. The actual reply itself will be the text I can train a NLP model on, and the timestamp can be used for a ML model to train relative to the date that managers are sacked. 

**Will there be enough data?**

This might be the most tedious part as I will have to cross track the dates that managers are sacked with the twarc request to pull that data. I also need to find examples of managers in bad form who aren't being sacked (eg. Liverpool) to see how that language differs, and teams who are in good form and don't need to be sacked(eg. Arsenal).

**Will there be problems with the data**

It would be asking to much of a ML to predict the exact date of when a manager is sacked. I want to create a threshold to see if it can predict within 30 days of the sacking and then try again at 15 days etc. There is also the problem of language. Pulling data from clubs outside of England will create replies that aren't in English which would be a problem for the English tokenizer. This means I can only pull data from English clubs or foreign clubs with a seperate English twitter account.

**What do you hope to get out of this?**

This model could be useful for people who don't follow every club, but still care enough about the sport to stay informed about the pressure on certain managers, and tune in to see "must win games." On a more personal level, this project will use a lot of skills that can be implemented into my future work as an analytical consultant.


## To Do

 - Find dates of managers who have been sacked.
 - scrape data from social media platforms to create a dataset from many different clubs. Ideally this should be about 40% sacked 60% not to get a representation of the normal sackings per season.
 - Create NLP to do sentiment analysis on the data set.
 - Create a ML algorithm to predict when a manager will be sacked based on dates of sentiment analysis.
 - Export into a medium of information applicable to sharing results.
