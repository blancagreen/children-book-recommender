# Children's book recommender

## CONTENTS OF THIS FILE

* Introduction
* Requirements
* Notebooks

## INTRODUCTION

This is a final project for the AllWomen Academy Data Science Inmersive Course, ending in July 2021.
The recording of the presentation is available [here](https://www.youtube.com/watch?v=Ke0LeeY-LK8&t=3413s) and a pdf file of the slides is included in this repository.

The goal of this project was building a book recommender for children following two different approaches, the Item-Item based and the Content based, after first steps of EDA and Data Cleaning.  
A gender analysis of a sample of the data was also carried out to conclude that the data was balanced before building the recommendation systems.

The original datasets used for this purpose have been downloaded from this [site](https://sites.google.com/eng.ucsd.edu/ucsdbookgraph/home).  
The data was collected by Mengting Wan and Julian McAuley in late 2017 from goodreads.com (with an update in 2019), scraping only users' public shelves.
Its use is only valid for academic purposes.

Their original papers can be found here:  

Mengting Wan, Julian McAuley, ["Item Recommendation on Monotonic Behavior Chains", in RecSys'18.](https://www.google.com/url?q=https%3A%2F%2Fgithub.com%2FMengtingWan%2Fmengtingwan.github.io%2Fraw%2Fmaster%2Fpaper%2Frecsys18_mwan.pdf&sa=D&sntz=1&usg=AFQjCNGGcNRW1tSZKPWO0yZsr8mj7MkWuw) [bibtex]  

Mengting Wan, Rishabh Misra, Ndapa Nakashole, Julian McAuley, ["Fine-Grained Spoiler Detection from Large-Scale Review Corpora", in ACL'19.](https://aclanthology.org/P19-1248/) [bibtex]  



## REQUIREMENTS

The datasets used in this project:  

[goodreads_books_children.json](https://drive.google.com/uc?id=1R3wJPgyzEX9w6EI8_LmqLbpY4cIC9gw4), containing 124,082 children books.

[goodreads_reviews_children.json](https://drive.google.com/uc?id=1908GDMdrhDN7sTaI_FelSHxbwcNM1EzR), containing 734,640 reviews.  

The environment's requirements list is included in the repository.

In order to skip some of the notebooks or avoid running some of the functions included in them that take time to complete, the related csv files can be downloaded from this [drive folder](https://drive.google.com/drive/folders/15mh-T6gA9I4ApwLub98o-v9xT45oHWJc?usp=sharing). To avoid changing a lot of paths, they should be stored in the notebooks'folder.


## NOTEBOOKS

### The project is divided into 6 notebooks:

- NOTEBOOK 1_DESCRIPTIONS_DF_EDA  

  It contains a first EDA and Data Cleaning of the goodreads_books_children dataset. There are two files in the drive folder, 
  booksdescriptiondetect.csv and bookstitledetect.csv that can be used to avoid running the language detection function.  



- NOTEBOOK 2_REVIEWS DF EDA & MERGING WITH DESCRIPTION DF

  It contains EDA and Data Cleaning of the goodreads_reviews_children dataset, and the merge with the clean dataset from notebook 1.  
  To avoid running the language detection function, use the file reviews_langdetect.csv included in the drive folder.  



- NOTEBOOK 3_WEBSCRAPING AND CREATING THE 1000 AUTHORS AND GENDER DF

  It contains the code to scrape from goodreads, the authors of the 1000 most popular books in the dataset, and the gender of those authors.  

  To avoid running the scrape_authors function, the file pop1000authorsfind2.csv is included in the drive folder. 

  The file 27authorsupdated from the drive folder contains 27 names added manually after the scraping.

  The file gender2.csv from the drive folder can be used instead of running the genderize function.    



- NOTEBOOK 4_DATA ANALYSIS OF DESCRIPTIONS AND REVIEWS 

  It contains wordclouds, sentiment analysis or topic modelling. In order to avoid running slow sentiment analysis functions, 
  the files Female_sentiment.csv and Male_sentiment.csv present in the drive folder can be used.  


 
- NOTEBOOK 5_BOOK RECOMMENDER 1 COLLABORATIVE FILTERING
 
  Item- item based recommender to make predictions about the interest of a user by collecting taste information from many other users.   
 


- NOTEBOOK 6_BOOK RECOMMENDER SYSTEM 2 CONTENT BASED DESCRIPTIONS AND REVIEWS  

  It considers the content of the books' descriptions and reviews in order to make predictions.

