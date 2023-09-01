# air_bnb_mid_project


Berlin Airbnb Ratings and Reviews Overview

Data Source: https://data.world/makeovermonday/2019w25 through https://www.kaggle.com/datasets/thedevastator/berlin-airbnb-ratings-and-reviews-overview by Andy Kriebel 

Installations
pip install langdetect
pip install vaderSentiment
pip install transformers
pip install wordcloud matplotlib

Files needed
air_bnb_Project_cleaning.ipynb
General_Analysis.ipynb
district_analysis.ipynb
Comment_sentiment_analisys.ipynb
Airbnb Berlin.csv

Order of running - Data Collection
Run first air_bnb_Project_cleaning.ipynb and then the other .ipynp files. Alternatively, you can download cleaned_Airbnb_Berlin.csv and skip running air_bnb_Project_cleaning.ipynb.


Linguistic Analysis and Sentiment Analysis:
- I calculated the review language distribution filtering the 2000 best rated properties against the 2000 least rated accomodations. For the language detection I used langdetect.
- For the sentiment Analysis, I cleaned the column 'comments' interpreting the encoded special characters and used the library vaderSentiment
- For the I excluded the most common grammatical words both in English and in German. No other data preparation was done. 

District Variation Analysis:
- For the district variation analysis, I grouped the dataset rows per listing_id, so for properties, to avoid that accomodations that have more reviews gained more weight in the analysis. I filtered out the neighboorhood-groups that had less reviews into other. I compared and plot the main statistics and distribution about the accomodation ratings per district. For the review language distribution per district, I used the detect method from langdetect.

Results:
- The variation in ratings both numerical and sentiment in this kind of data is extremely limited.
- Mitte performed relatively particularly bad.
- The numerical rating matches with the linguistics model. In both cases a very limited difference can differentiated a good accommodation from a mediocre one.
- Most rated accommodation reviews tend to have more intensifiers, and least rated accommodation reviews are distinguished by a slightly more proportion of neutral tone.


Future Improvements:
- Further research: direct correlation between satisfaction scores and income.
- Refining the sentiment analysis.


Acknowledgments:
Data Source from Andy Kriebel - https://data.world/makeovermonday/2019w25 through https://www.kaggle.com/datasets/thedevastator/berlin-airbnb-ratings-and-reviews-overview by Andy Kriebel 
