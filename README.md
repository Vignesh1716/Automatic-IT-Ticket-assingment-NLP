# Automatic-IT-Ticket-assingment-NLP
AI based model using NLP for assigning the ticket to correct functional team based on the given description in mail

 
During the process of tickets assignments by L1 / L2 teams to functional groups, there were multiple instances of ticketss getting assigned to wrong functional groups. Around ~25% of tickets are wrongly assigned to functional teams. Additional effort needed for Functional teams to re-assign to right functional groups. During this process, some of the tickets are in queue and not addressed timely resulting in poor customer service. 

Guided by powerful AI techniques that can classify incidents to right functional groups can help organizations to reduce the resolving time of the issue and can focus on more productive tasks. 

# Objective
Our objective here is to build an AI-based classifier model to assign the tickets to right functional groups by analysing the given description with an accuracy of at least 85%.

# Steps followed
Text in Description is pre-processed by removing unwanted characters and words. Some descriptions are given in other languages which are translated to english internally. Stop words are removed and all the words are lemmatized.

With this pre-processed description the words in the corpus are tokenized and embeddings were created with word2vec. Embedding was also generated with glove.

Different NLP algorithms were tried out - BI-LSTM, LSTM,Traditional ML algorithms such as NB were tried out.
# Limitations
Except Grp_0, other groups are not having enough datapoints, we are not able to derive a model to reach 100% accuracy. Before applying this model into production, either additional datapoints are required from business team or additional manual intervention could help achieve higher accuracy.  
# Closing Reflection
Looking at the data points, looks like short description and description fields were manually entered and hence were having data entries with German language or with email addressed, special characters etc. and hence data cleansing becomes a critical task in entire predictability of target group. 
To avoid this issue of data cleansing, it is recommended to have an unified port for raising such tickets e.g. My Support Portal which helps team to capture right amount of contextual data and ultimately helps NLP model to perform better in classifying ticket to correct group.
