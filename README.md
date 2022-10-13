
# (Twitter WeRateDogs Data Wrangling & Analysis)
## by (Kommomo Usang)


## Dataset

This project  utilized datasets from the tweet archive of Twitter user @dog_rates, also known as WeRateDogs- a Twitter account that rates people's dogs with a humorous comment about the dog. These ratings have a numerator of 10 and WeRateDogs has over 4 million followers and has received international media coverage. Data Wrangling and analysis were performed on 3 datasets of twitter from the tweet archive of Twitter user @dog_rates. These datasets are named twitter_archive_enhanced.csv, image-predictions.tsv and tweet-json.txt. 

The twitter_archive_enhanced csv file stores information on the WerateDogs twitter archive
The image-predictions tsv file stores information on the kind of dog present in each tweet according to a neural network. It is hosted on Udacity's servers and i downloaded it programmatically using the Requests library and the following URL: https://d17h27t6h515a5.cloudfront.net/topher/2017/August/599fd2ad_image-predictions/image-predictions.tsv
The additional data from the tweeter API is stored in a tweet-json txt file and i downloaded from Udacity's link- https://video.udacity-data.com/topher/2018/November/5be5fb7d_tweet-json/tweet-json.txt as my application for a twitter developer account was still under review.

Each of these datasets which are tweet data have characteristics of big data making them have data quality and tidiness issues as was seen by their data quality and tidiness issues. In a bid to inspect these dataset and fix these issues i put these datasets through the wrangling process in a 3-fold step summarized as -Gather Assess and Clean. The result of this process was a cleaned dataset merged from the 3 datasets to one dataset. By the end of the cleaning process, they are merged into one dataset file called twitter_werate and then stored in a file called twitter_archive_master.csv. This dataset consists of 1954 entries with all the detected quality and tidiness issues resolved

## Installation

To be able to run this code, you will need the following-
- jupyter notebook
- Installation of the following anaconda package libraries- pandas, numpy, requests, tweepy, json, dataset files(.csv,.txt, .json)

## Summary of Findings

> I explored my wrangled data determine what factors influence high ratings of dogs. My chosen dependent variable was rating_denominator(rating) and Independent variables were source and dog_stage. The following findings were made -
- The source with the highest number of tweets is Twitter for iphone with 1915 tweets out of 1954 tweets.
- pupper dog stage has the highest number of tweets with 201 tweets out of 303 tweets, followed by doggo and puppo with 63 and 22 respectively
- The top rating is 12/10 with 446 tweets, followed closely by 10/10 and 11/10
- There is a strong correlation between ratings and dog_stage as the combination of pupper dog_stage and 12/10 rating have the highest number of tweets. Hence, dog_stage strongly influnces the rating of the dog.
- There is no correlation between ratings and source. This implies that the tweet source does not influence the rating of the dog
