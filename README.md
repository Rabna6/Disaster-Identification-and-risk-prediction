# Disaster-Identification-and-risk-prediction

DISASTER IDENTIFICATION AND RISK PREDICTION USING DEEP LEARNING
Data Science Product Development– SPRING 2021
UM-E-RABNA BAJWA
ERP – 23374

-	PROJECT DOMAIN:

This project aims to develop an understanding and reporting of risks about Natural Disasters. Social media is increasingly being used to broadcast useful information during local crisis situations (e.g. hurricanes, earthquakes, explosions, bombings, etc). Identifying disaster related information in social media is challenging. In this project, I will use tweeter data and deep learning to address this challenge.

-	BACKGROUND KNOWLEDGE:

	Early-warning systems play a pivotal role in the reduction of risks related to natural hazards. However, early warning is usually not available or practicable for mitigating risks. Warning times for some natural hazards are often very short and might prove to be insufficient for taking preventive action at hazardous installations.
	Every year, Natural Disasters result in infrastructural damages, monetary costs, distresses, injuries and deaths. Unfortunately, climate change is strengthening the destructive power of natural disasters. In this context, Disaster risk analysis and predicting system will help to cope with disasters and emergencies by improving the disaster detection and search and rescue missions during disaster response.
	For instance, the tsunami that hit Japan in March 2011, destroyed more than 120,000 buildings and occasioned an estimated ﬁnancial damage of about $199billion dollars, and caused 15,894 deaths
	In Canada, the Fort McMurray wildﬁre forced over 88,000 people to leave their town and caused an estimated C$3.6 billion of insurance costs and also destroyed about 10% of all structures in the town and provoked chaos with people leaving their home with whatever they could take.
	For instance, the tsunami that hit
	Japan in March 2011, destroyed more than 120,000 buildings,
	occasioned an estimated ﬁnancial damage of about $199
	billion dollars, and caused 15,894 deaths

-	PROJECT DEFINITION: 
For identifying the type and risk of natural disasters we will make use of tweets that are sent from mobile devices and can be geotagged containing the precise location coordinates. However, only about 1% to 3% of all tweets are geotagged. Identifying the disaster-related tweets along with their actual geolocations is highly valuable for the first responders in disaster and crisis situations. In this project, we first identify the disaster-related tweets using a deep learning model and subsequently use a Named Entity Recognition model to identify and extract the name of the places (cities, countries, etc.) from the tweets, and finally use a geoparser model to identify the geo-location of the events on the map. We should emphasize that geo-location identification is a critical step as we can’t simply use the location of the tweets provided by the tweeter API for disaster identification purposes. The location of the person who tweets about a disaster is not necessarily identical to the actual location of the events. A user could be located in New York but tweets about a flood happening in another place like Kansas.  

-	DATASETS:
For addressing the above problem, I have used the CrisisLexT6 dataset which includes Tweets from six crises, labeled by relatedness.
The data from the following crisis events were used in this project:
•	Flood
•	Earthquake
•	Hurricane
•	Tornado
•	Explosion
•	Bombing
•	Wildfire


-	PROJECT CONTENTS:
1.	Reading & Understanding the data
A.	Importing the input files
B.	Inspect Data Frames
2.	Data Preprocessing
A.	Data Loading
B.	Data Cleaning and Manipulation
C.	Re-sampling
3.	Data Transformation
A.	Tokenization
B.	Padding
C.	Label Encoding
D.	One Hot Encoding
E.	Word Embedding
F.	Training Test Dataset
4.	Data Modeling
A.	Model Architecture
B.	Training
C.	Evaluation
D.	Prediction
E.	Hyper parameter Optimization




-	PROJECT WORKING AND CONCLUSION:
-	The project initiates with the data collection and cleaning process. The backend API uses a keyword-based sampling approach to collect tweets using Twitter’s streaming API. In this project a reference dictionary of disaster related terms was used as keywords. The relevant tweets mention different types of disasters between October 2012 and July 2013 in the US, Canada, and Australia.
-	The API then sends the tweet to the deep learning model built using TensorFlow 2.0 for Python and exposed as a Flask app. The model analyzes the textual content of tweets to evaluate their relevance to floods, earthquakes, hurricanes, tornadoes, explosions, and bombings. The relevant tweets are then sent to the geoparser, which extracts place names from the text and geocodes them. Lastly, the results indicate tweets that provide timely information regarding the incident locations and impacts of the ongoing event.

-	FUTURE WORK:

The current model uses Twitter as the only source of information. Although the results are promising, the integration of other sources of information such as official news outlets and other social media platforms would be beneficial to improve the data validation process so as to achieve more realistic results. Moreover, the project only uses textual content for detecting disaster events and ignores the visual content (photos/videos). But we can further add analysis of visual content in social media messages that can provide contextual information and contribute to crisis mapping of the situation.



