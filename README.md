# SOSC314-PROJECT-Media presentation and public opinion toward ICE on Youtube
#Zijin
#Xiaoye

**PART I Motivations**

  During last Thanksgiving, one project member witnessed protesters hoding "ICE out of RDU" signs alongside the highway from Raleigh to Durham. This first-hand witnessing of protest against activity of Immigration and Customs Enforcement(ICE) aligns with the escalating public debate over immigrantion issues,civil rights and the exercise of statepower. Data from the Wayback Machine indicates that public attention towards ICE reached an unprecedented historical peak in December 2024.This tension was undoubtly ignited by the recent shooting in Minnesota on Jan.7th, exacerbating the inherent conflicts between local and federal agencies, citizens and the state apparatus, as well as divergences between political ideologies.
  <img width="3075" height="1458" alt="bd78b5d327e2251f230ecbfaf1730c34" src="https://github.com/user-attachments/assets/21fa708d-cf9f-4f7b-9ea5-02e8f03da234" />

**PART II Research Question**
1.What are the primary themes in media coverage and public discourse surrounding ICE-related events?
2.To what degree are ideological and sentimental divergents showcased in online ICE related discusions? Are these divergents align with media discourses?  

**PART III Data Source**

***a.Platform, Channel and Time Selection***

  We selected YouTube, the world's largest stream media extensive news coverage, as our primary data source, as our primary data source.This choice is justified by the immense scale and depth of engagement on this platform. When searching "ICE Minnesota" as a topic term on YouTube, numerous videos have garnered millions of views and thousands to tens of thousands of comments, indicating exceptionally high public attention and engagement with this topic on this platform. This provides abundant data for our research, ensuring a sufficient sample size for analyzing public opinion and media framing.
  We selected the YouTube channel of CNN and Fox news as two sources, as they are two mainstream medias with contrasting ideological stances and high audience engagement, which provides rich potential data to answer our RQs.
  We collected videos from 2025/01/01, for Trump's second term stimulated the activity of ICE and people's raising attentions.
  
***b.Data Collection***

  We used package yt-dlp to collect all videos under CNN & Fox channels during 2025/01/01 and 2026/1/21 whose title includes the word “ICE”. 
  We collected 66 videos from CNN with video id,	title,	upload date,	view count, description and transcript, together with 141372 comments with user id, timestamp and like count. 
  We collectede 62 videos and 125222 comments for Fox news using the same codes. 
  All data was sorted into csv files.
  
**PART IV the unit of analysis**

1.Temperal analysis on development of ICE related events and online discussions, especially before and after the shoot in Minnesota, focusing on overall trend and transition.  
2.Text analysis on video content produced by selected media cooperations, exploring potential discursive strategies and ideological orientations.  
3.Text analysis on comment under selected videos, exploring public sentiment, perception on ICE as a federal institution, and ideological orientations.  

**Quick Links**
[Data](./data/): 100+ video transcripts & 280000+ comments with metadata collected from official YouTUbe channel of CNN and Fox news.
[Codes](./codes/):Scripts for data scraping, data cleaning, word frequency, topic modeling and emotion analysis
[Tables](./Tables/):Calculated results for word frequency, topic modeling and emotion analysis
[Figures](./Figures/):Visualized results for word frequency, topic modeling and emotion analysis

**Repository Structure**
│
├─Background
│      ICE_Timeline_textandimage.ipynb
│
├─codes
│  │
│  ├─1. data collection
│  │      CNN_data_collection.ipynb
│  │      comment_cleaning&xlsx_to_csv_code.
│  │
│  │─2. Adjusted_Frequency&_Topic_modeling_code.ipynb
│  ├─3. Emotion_analysis_and_DTM
│  │      cnn_anger_ice_strict_pipeline_py.ipynb
│  │      Sentiment_Analysis&_DTM_of_CNN_comment.ipynb
│  │      Sentiment_Analysis&_DTM_of_FOX_comment.ipynb
│  │
│  └─4. Structural_Topic_Modeling
│          CNN_STM_analysis_Final.Rmd
│          Fox 2stage STM analysis(final).Rmd
│          Fox-Ideal K.Rmd
│          readme
│
├─data
│      CNN_Comments_Final.zip
│      CNN_Video_Final.csv
│      Fox_Comment_Details.csv
│      Fox_Video_Summary.csv
│
├─Figures
│      CNN_Comment_emotion_distribution.png
│      CNN_Comment_emotion_distribution_proportion.png
│      CNN_comment_lemmatized_FREX_Words.png
│      CNN_comment_Topic_Engagement.png
│      CNN_comment_Top_15_quality_topic_vis.png
│      Fox_Comment_emotion_distribution.jpg
│      Fox_Comment_emotion_distribution_proportion.png
│      Fox_comment_lemmatized_FREX_Words.png
│      Fox_comment_Topic_Engagement.png
│      Fox_comment_Top_15_quality_topic_vis.png
│
└─Tables
        CNN_Emotion_DTM_Analysis_Results.zip
        CNN_frequency_top_50_words_revised.csv
        CNN_STM_Topic_FREXwords_Summary_10.csv
        FOX_Emotion_DTM_Analysis_Results.zip
        Fox_frequency_top_50_words.csv
        Fox_STM_Topic_words_Summary_10.csv
