# SOSC314-PROJECT
#Zijin
#Xiaoye

**PART I Motivations**

  During last Thanksgiving, one project member witnessed protesters hoding "ICE out of RDU" signs alongside the highway from Raleigh to Durham. This first-hand witnessing of protest against activity of Immigration and Customs Enforcement(ICE) aligns with the escalating public debate over immigrantion issues,civil rights and the exercise of statepower. Data from the Wayback Machine indicates that public attention towards ICE reached an unprecedented historical peak in December 2024.This tension was undoubtly ignited by the recent shooting in Minnesota on Jan.7th, exacerbating the inherent conflicts between local and federal agencies, citizens and the state apparatus, as well as divergences between political ideologies.
  <img width="3075" height="1458" alt="bd78b5d327e2251f230ecbfaf1730c34" src="https://github.com/user-attachments/assets/21fa708d-cf9f-4f7b-9ea5-02e8f03da234" />

**PART II Research Question**

To what extent did the Minnesota shooting trigger a shift in public opinions regarding ICE on YouTube, and how do the temporal evolutions of ICE related online discussions reflect public perceptions of state repressive power and political polarization?

RQ1 (Impact): Does the Minnesota shooting represent a significant causal breakpoint in the volume, sentiment, and thematic focus of ICE-related discourse over time?  
RQ2 (Legitimacy): Does public perception on ICE's legitimacy as a federal institution changed overtime?  
RQ3 (Polarization): To what degree are ideological and sentimental divergents showcased in online ICE related discusions? Are these divergents align with media discourses?  

**PART III Data Source**

***a.Platform Selection***

  We selected YouTube, the world's largest stream media extensive news coverage, as our primary data source, as our primary data source.This choice is justified by the immense scale and depth of engagement on this platform. When searching "ICE Minnesota" as a topic term on YouTube, numerous videos have garnered millions of views and thousands to tens of thousands of comments, indicating exceptionally high public attention and engagement with this topic on this platform. This provides abundant data for our research, ensuring a sufficient sample size for analyzing public opinion and media framing.

***b.Video Selection***
  
  We are still exploring effective way of selecting specific videos for data collections. Here are two potential directions:
  
  1.Determine a list of certain terms relating ICE issues for searching,eg "ICE minnesota"; searching these term and filter according to view counts; identifying corporate media channels showing up; looking into all ICE related videos under these channels.  
  2.Get videos from specific hashtag related to ICE, eg "ICE shooting"; look into both videos from media channels and shorts.
  
***c.Types of data to be collected***

  We plan to scrape the following data points from relevant videos:
  
  *1.Video content*: Titles, transcripts  
  *2.Metadata*: Channel names, publication dates, view counts, like/dislike ratios    
  *3.User comments*: Comment text, timestamps, vote counts, secondary comments  
  
**PART IV the unit of analysis**

1.Temperal analysis on development of ICE related events and online discussions, especially before and after the shoot in Minnesota, focusing on overall trend and transition.  
2.Text analysis on video content produced by selected media cooperations, exploring potential discursive strategies and ideological orientations.  
3.Text analysis on comment under selected videos, exploring public sentiment, perception on ICE as a federal institution, and ideological orientations.  

**PART V  data feasibility assessment**

Using yt-dlp package, auto-generated captions(English), metadata(time, views, votes) and comments of videos from certain channels and certain tags are accessible.
<img width="1914" height="668" alt="image" src="https://github.com/user-attachments/assets/7b9b6bf6-e0c9-4695-acfe-1fade6d0ac69" />
<img width="615" height="767" alt="image" src="https://github.com/user-attachments/assets/afa8ea11-8231-4d70-89b5-8f5580c556b0" />

