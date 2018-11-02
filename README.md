# Youtube-Community-Toxicity
For the final project (AKA capstone) of my data science intensive I decided to attempt to use sentimentalization to discover evidence of and correlations to toxicity or supportiveness of the cultures of individual youtube channels.  

## Problem Statement  
Through sentimentalization, can we learn which channels have the most positive and negative communities?  The metric by which the sentiment is measured is represented by a number between -1 and 1, in which numbers closer to -1 are more negative and numbers closer to 1 are more positive.

## Relevance
By identifying which channels are putting out more positivity and which are putting out more toxicity, youtube and other platforms might be able to assist creators in improving on such things if they wish to do so.  This would help Youtube support the channels which or more positive, which in turn could help improve the brand of Youtube by making it present more as a place which can foster positivity rather than a cesspool of potential negativity.

## Data Collection
The data was originally collected with a small selection of channels and videos.  Over time the collection expanded when able.  The data was collected from the youtube API.  The data can be found in this repo in the file marked "data".

## EDA
With the main thrust of the experimentation being sentiment analysis, it was important to start with a baseline of the sentiment of the channels collected.  The sentiment analyzer that was used was imported from the textblob library, which was trained on reviews rather than community interactions.

|Channel               |Sentiment|
|----------------------|---------|
|Aliens_Guide          |0.320    |
|Everyman_HYBRID       |0.272    |
|Hi_Im_Mary_Mary       |0.297    |
|LaRon_Readus          |0.294    |
|Maggie_Mae_Fish       |0.345    |
|MovieBob              |0.281    |
|NerdSync              |0.298    |
|Nyx_Fears             |0.328    |
|Petscop               |0.254    |
|Sammus                |0.356    |
|Small_Beans           |0.312    |
|Some_More_News        |0.292    |
|Strange_Aeons         |0.266    |
|Super_Bunnyhop        |0.269    |

## Modeling
The purpose of modeling in this situation was to give us an idea of what correlations can be inferred from the sentiment of channels and videos.  Unfortunately, the starting models were impractically terrible and the data that was originally scrapped wasn’t complete enough to give an accurate idea of correlation to sentiment.

## Future Steps
The future steps include obtaining even more data and attempting to randomize the data collection.  Another step would be to gather information related to the type of content that youtube has assigned the channel.  This might be able to show some correlation between broader content and the sentiment generally found from that content.  Furthermore, it would be valuable to get some basic demographic data from the content creators such as gender and age.  Another important factor to look into might be political leaning. What might be gleaned by comparing democratic and republican leaning channels?  News channels in general might be enlightening, especially when removing politics from what’s being reported to leave such things as emerging technology or small stories that are being covered.
Another potential would be to locate data that might already be labeled as toxic or supportive and then training a sentiment analyzer on that data.  This would allow a better accuracy than correlating general positivity and negativity as instead of being trained on reviews, it would be trained on the behavior of people who are being blatently toxic and potentially subtly toxic as well.  If one could obtain the data of reported documents (tweets, comments, posts, etc) then one could easily have a starting point for the negativity end of the spectrum.  This would likely be more difficult than obtaining supportive community sentiment.
