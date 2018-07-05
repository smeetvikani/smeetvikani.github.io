![Sklearn logo](http://downloadforpc.net/Metis/facial_rec/logo.jpeg)

### Table of Contents
[1. Project Overview](#section-a)  
[2. App Demo](#section-ba)  
[3. Tools Used & Workflow](#section-b)  
[4. Data Collection](#section-b2)  
[5. Modeling: NLP Processing](#section-c)    
[6. Lyrics Based Recommendation](#section-ca)     
[7. Github Repo - Link](https://github.com/smeetvikani/Photo_to_Playlist)

---

### <a name="section-a"></a>1.  Project Overview

#### “Emotion Based music recommendation with facial detection.”

Designed an app that will take in an input image and output a recommended playlist based on emotions of the users.  

##### The 3 goals for this project are:
1.  Classify Emotions in a Given Picture Real Time
2.  Use emotions to generate and recommend playlist for the user.
3.  Create an app that would generate one unique playlist for each picture.

### <a name="section-ba"></a>2. App Preview: 

<iframe width="560" height="315" src="https://www.youtube.com/embed/WxvRlYI7VJk" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
<br>
Demo for the app Available at: 
[Link to App Demo](www.selfiemixtape.com)
<br>

---

### <a name="section-b"></a>3.  Tools Used and Workflow:

###### Python, Sklearn, TSNE, Word2Vec, Flask, S3, Amazon Rek, EC2, MongoDB, Pandas, Matplotlib and Seaborn, Jupyter Notebook, HTML, CSS. 
![Sklearn logo](http://downloadforpc.net/Metis/facial_rec/workflow.jpeg)

<br>

---

#### 3. Project Timeline: 
![Sklearn logo](http://downloadforpc.net/Metis/facial_rec/timeline.jpeg)
<br>
<br>
---
### <a name="section-b2"></a>4.  Data Collection
Raw JSON data was collected from AWS Rekognition interface for each picture and saved to MongoDB.

Lyrics Data was scraped from AZLyrics.com and song features were scraped from Spotify. A collection of 350K songs with features were inserted into a MongoDB. 
<br>
---
### <a name="section-c"></a> 5. NLP Processing (Lyrics)
##### Phase 1: Used GloVe Corpus (Global Vectors for Word Representation - Stanford NLP) 
Stanford University NLP Department put the corpus together by extracting word context from 28B tweets Corpus consisted of 1.2M words in 100 Dimensional Vector Space. 

I Collected vectors for each word in each song from the 1.2M word corpus. Then, averaged the vectors for all the words in 1 song. 
As a result, was able to produce the following plot for which each vector on this TSNE plot represents a song. 

![Sklearn logo](http://downloadforpc.net/Metis/facial_rec/tsne.jpeg)
<br>

### <a name="section-ca"></a>6. Lyrics Based Recommendation
For each song in a 100D vector space. Used Cosine Distance to calculate the distance between the emotion and the song. Below is the list of emotions used for this project. 

###### Emotion list: Happy, Sad, Angry, Confused, Stunned, Calm, Annoyed
![Sklearn logo](http://downloadforpc.net/Metis/facial_rec/cosine.jpeg)
<br>

For Example, based on the lyrics one song has a distance associated with each emotion. Lower the distance the better. Using this tactic, I was able to leverage gradiance of emotions to recommend a playlist. As a result, I am able to produce a unique playlist for each picture. 

<br>

### <a name="section-end"></a> Contact:
Thank you for visiting my blog, If you have any questions free to contact me at smeet.vikani@gmail.com


