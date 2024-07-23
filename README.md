# QTM-302W
--
title: "R Notebook"
output: html_notebook
---

Components of Analysis (from canvas, basically the rubric for the assignment)
* Introducing the dataset (including its source, scope, and any ethical considerations) framed by the purpose of the exploratory analysis, anticipating any subsetting or re-ordering of the data for your interests
* Reading the data into R in a tabular format, identifying, subsetting, and renaming the variables for your use
* Forming the core data frame that you'll be working from by reshaping and summarizing the data, storing new data frames in memory where appropriate
* Cleaning the data according to your purpose for the dataset
* Plotting distributions of your data
* Calculating basic statistical metrics like central tendency measures
* Some light correlational analysis/visualization of key variables.
* A look forward to what further questions the analysis suggests and what it enables

# Music Dataset : 1950 to 2019

## Introduction

In a nutshell, our dataset collects music produced from 1950 to 2019, fetched from Spotify. We obtained the dataset from Kaggle (DOI: 10.17632/3t9vbwxgr5.3), where the description said, "This dataset provides a list of lyrics from 1950 to 2019 describing music metadata as sadness, danceability, loudness, acousticness, etc. Authors also provide some information as lyrics which can be used to natural language processing." Our purpose TKTK (after we decide on the question to support further exploration).

We first load the dataset and the tidyverse package in preparation for further exploration.

```{r}
#Load the `tidyverse` package
pacman::p_load(tidyverse)

#Load the `music` dataset which is the csv file tcc_ceds_music
data(tcc_ceds_music)
```

We then apply head(), str(), and summary() to obtain an overview of the dataset.

```{r}
#Print the first 6 observations
head(tcc_ceds_music)
```


```{r}
# Counting unique values in the "track_name" column
unique_tracks <- unique(tcc_ceds_music$track_name)
num_unique_tracks <- length(unique_tracks)

# Print the number of unique tracks
print(num_unique_tracks)
```

Below is the code for a Boxplot with a color gradient

```{r}
install.packages("ggplot2")
install.packages("dplyr")
install.packages("magrittr")
library(ggplot2)
library(dplyr)
library(magrittr)

medians <- tcc_ceds_music %>%
  group_by(genre) %>%
  summarise(median_danceability = median(danceability, na.rm = TRUE))

tcc_ceds_music <- tcc_ceds_music %>%
  left_join(medians, by = "genre")

ggplot(tcc_ceds_music, aes(x = genre, y = danceability, fill = median_danceability)) +
  geom_boxplot() +
  scale_fill_gradient(low = "blue", high = "red") +
  theme(axis.text.x = element_text(angle = 90, hjust = 1)) +
  labs(title = "Box Plot of Danceability Scores by Genre",
       x = "Genre",
       y = "Danceability",
       fill = "Median Danceability")
```
