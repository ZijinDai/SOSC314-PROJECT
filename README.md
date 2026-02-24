# Analyzing Media Presentation and Public Opinion toward ICE on Youtube
#Zijin
#Xiaoye

## Project Motivations

  During last Thanksgiving, one project member witnessed protesters hoding "ICE out of RDU" signs alongside the highway from Raleigh to Durham. This first-hand witnessing of protest against activity of Immigration and Customs Enforcement(ICE) aligns with the escalating public debate over immigrantion issues,civil rights and the exercise of statepower.   
  Data from the Wayback Machine indicates that public attention towards ICE reached an unprecedented historical peak in December 2024.This tension was undoubtly ignited by the recent shooting in Minnesota on Jan.7th, exacerbating the inherent conflicts between local and federal agencies, citizens and the state apparatus, as well as divergences between political ideologies.
  <img width="3075" height="1458" alt="bd78b5d327e2251f230ecbfaf1730c34" src="https://github.com/user-attachments/assets/21fa708d-cf9f-4f7b-9ea5-02e8f03da234" />

## Research Questions
1. What are the primary themes in media coverage and public discourse surrounding ICE-related events?  
2. To what degree are ideological and emotional divergences showcased in online ICE related discusions? Are these divergences align with media discourses?  

## Data Source

***a.Platform, Channel and Time Selection***

  We selected YouTube, the world's largest stream media extensive news coverage, as our primary data source, as our primary data source.This choice is justified by the immense scale and depth of engagement on this platform. When searching "ICE Minnesota" as a topic term on YouTube, numerous videos have garnered millions of views and thousands to tens of thousands of comments, indicating exceptionally high public attention and engagement with this topic on this platform. This provides abundant data for our research, ensuring a sufficient sample size for analyzing public opinion and media framing.
  We selected the YouTube channel of CNN and Fox news as two sources, as they are two mainstream medias with contrasting ideological stances and high audience engagement, which provides rich potential data to answer our RQs.
  We collected videos from 2025/01/01, for Trump's second term stimulated the activity of ICE and people's raising attentions.
  
***b.Data Collection***

  We used package yt-dlp to collect all videos under CNN & Fox channels during 2025/01/01 and 2026/1/21 whose title includes the word “ICE”. 
  We collected 66 videos from CNN with video id,	title,	upload date,	view count, description and transcript, together with 141372 comments with user id, timestamp and like count. 
  We collectede 62 videos and 125222 comments for Fox news using the same codes. 
  All data was sorted into csv files.
  
## Units of analysis

***a.Video Content(Transcript)***
1. Word Frequency: most frequently mentioned words in video transcripts
2. LDA Topic Modeling: clustered main topics from video transcripts using the Gensim package

***b.Comments***
1. Structural Topic Modeling:analyze main topics from comments together with engagements(likecounts)
2. Emotion analysis: utilized the Hugging Face DistilRoBERTa-base model to categorize comment emotions; identified stances of comments catagorized into "anger"
   
## Main Findings 
Our analysis reveals a clear divergence in framing between the two media outlets and their respective audience reactions:

1. Media Outlet Perspectives (Framing)
CNN: Primarily reports from an immigration-centric perspective, focusing on specific humanitarian events and individual cases.
Fox News: Predominantly adopts a law enforcement perspective, framing the narrative around border security and legal procedures.

2. Common Themes in Audience Comments: audiences from both channels express high levels of frustration with corruption and the perceived failure of governmental institutions.

3. Divergent Stances in Comments  
Target of Dissatisfaction:  
CNN Audiences: Exhibit a significantly higher rate of opposition toward ICE agents (~88%,40% higher than that under Fox)   
Fox News Audiences: Direct their dissatisfaction primarily toward local government failures and perceived corruption in municipal leadership.

4. Engagement of topics:  
   CNN Audiences:high engagement(likecounts) in specific cases(eg: shootings in Minnesota, arrests in Hyundai factory...)  
   Fox News Audiences: engage more with dissatisfaction towards local governance in regions where ICE-related incidents occurred.

## 🔗 Quick Links

- 📂 [Data](./data/) – 100+ video transcripts & 280,000+ comments 
- 💻 [Codes](./codes/) – Scripts for scraping, cleaning, modeling 
- 📊 [Tables](./Tables/) – Word frequency, topic & emotion results 
- 📈 [Figures](./Figures/) – Visualized results 


## Repository Structure

```text
SOSC314-PROJECT/
├── README.md
├── Background/
│   └── ICE_Timeline_textandimage.ipynb
├── codes/
│   ├── Adjusted_Frequency&_Topic_modeling_code.ipynb
│   ├── data collection/
│   │   ├── CNN_data_collection.ipynb
│   │   └── comment_cleaning&xlsx_to_csv_code.ipynb
│   ├── Emotion_analysis_and_DTM/
│   │   ├── cnn_anger_ice_strict_pipeline_py.ipynb
│   │   ├── Sentiment_Analysis&_DTM_of_CNN_comment.ipynb
│   │   └── Sentiment_Analysis&_DTM_of_FOX_comment.ipynb
│   └── Structural_Topic_Modeling/
│       ├── CNN_STM_analysis_Final.Rmd
│       ├── Fox 2stage STM analysis(final).Rmd
│       ├── Fox-Ideal K.Rmd
│       └── readme
├── data/
│   ├── CNN_Comments_Final.zip
│   ├── CNN_Video_Final.csv
│   ├── Fox_Comment_Details.csv
│   └── Fox_Video_Summary.csv
├── Figures/
│   ├── CNN_Comment_emotion_distribution.png
│   ├── CNN_Comment_emotion_distribution_proportion.png
│   ├── CNN_comment_lemmatized_FREX_Words.png
│   ├── CNN_comment_Topic_Engagement.png
│   ├── CNN_comment_Top_15_quality_topic_vis.png
│   ├── Fox_Comment_emotion_distribution.jpg
│   ├── Fox_Comment_emotion_distribution_proportion.png
│   ├── Fox_comment_lemmatized_FREX_Words.png
│   ├── Fox_comment_Topic_Engagement.png
│   └── Fox_comment_Top_15_quality_topic_vis.png
└── Tables/
    ├── CNN_Emotion_DTM_Analysis_Results.zip
    ├── CNN_frequency_top_50_words_revised.csv
    ├── CNN_STM_Topic_FREXwords_Summary_10.csv
    ├── FOX_Emotion_DTM_Analysis_Results.zip
    ├── Fox_frequency_top_50_words.csv
    └── Fox_STM_Topic_words_Summary_10.csv
