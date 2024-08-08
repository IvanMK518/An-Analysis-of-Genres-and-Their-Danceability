“We should consider every day lost on which we have not danced at least once.”
― Friedrich Wilhelm Nietzsche

# Danceability: Breaking Down the Vague Concept

#### -- Project Status: [Completed]

## Project Intro/Objective
The purpose of this project is to define danceability, a vague term, with more concrete vocabs. Specifically, we want to identify a few correlations between danceability and other features of songs, which eventually allows people to play songs accompanying dancing based on a song's loudness, amount of instrumentality involved, etc. instead of looking for a specific index called "danceability," which is indeed hard to find on a lot of music platforms.

### Partner
* Ivan Martinez-Kay
* Daniel Nickas
* Sandy Ge

### Methods Used
* Data Cleaning
* Data Visualization
* Correlational Statistics

### Technologies
* R 

## Project Description
Dancing is something that comes naturally to our body, and it's hard to imagine, at least sometimes, dancing without the accompany of music. Therefore, it is natural to wonder the relationship between music and dancing. In other words, what features of a song add to its danceability? To transform the vaguely defined and measured "danceability" into more tangible terms like "instrumentality," "loudness," etc., this repository aims to identify a few noticeable correlations between danceability of a song with other features.

To give you an overview of the content this repository contains, you can find the dataset of which we have based our analysis on, a renv file which allows you to replicate the computing environment we have created, and most importantly, two versions of code notebooks which contain all our codes,  analysis, and the conclusions we have reached in regards of the relationship between the different features of a song and its danceability. In the end, we have find some common correlations, including but not limited to that low instrumentality, high feeling, and high loudness usually is correlated with higher danceability. 

We encourage others to read on and continue build on our analysis. One potential next step is to explore other features of songs from our dataset. The dataset we are using have more than 30 different measurements of songs, and we have only selected a few to clean and visualize. As a result, please feel free to copy and coding and reuse them on some of the other columns so that the next time someone is feeling like dancing, they can judge a song not only based on the qualities we have presented.

So far, we have concluded that high instrumentality, acousticness, and energy correlate to lower danceability. Loudness and and valence are directly proportional to danceability. This suggests that euphoric and lyrical music are most danceable, explaining why hip hop and reggae lead.

## Needs of this project

- data exploration/descriptive statistics
- data processing/cleaning
- statistical modeling
- writeup/reporting

## Directory Stucture

* Data
    * music.csv
* Markup
    * EDA_Code-Notebook_with_complete_code_and_narration.html
* R
  * EDA_Code-Notebook_with_complete_code_and_narration.rmd
* .DS_Store
* README.md
* renv.lock


## Getting Started

1. Clone this repo (for help see this [tutorial](https://help.github.com/articles/cloning-a-repository/)).
2. Raw Data is being kept in the data folder within this repo. 
3. Data processing/transformation scripts are being kept in the R folder within this repo.

## Contacts Info

|Name     |  Email   | 
|---------|-----------------|
|[Ivan Martinez-Kay]|ivan.martinez-kay@emory.edu|
|[Daniel Nickas]|daniel.nickas@emory.edu|
|[Sandy Ge]|sandy.ge@emory.edu|

* Feel free to contact us with any questions or if you are interested in contributing!
