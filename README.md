# CLEF 2021 - CheckThat! Task 1 on check-worthiness of Spanish tweets

This repository contains the dataset for the [CLEF 
2021-CheckThat!](https://sites.google.com/view/clef2021-checkthat) task 1 
Spanish. The task consists in ranking a stream of tweets according to their 
check-worthiness.

The data consists of tweets from Spanish politicians, annotated by professional 
human fact-checkers. 

* Only tweets with a certain degree of agreement between fact-checkers were 
selected.
* This version of the dataset is already divided into training and development 
sets (the blind test set will be released at evaluation time).
* All dataset partitions are provided in 3 formats: CSV , TSV (tab-separated 
values) and JSON. The first two are
  equivalent and contain the tweet text, the tweet ID and the label to be 
predicted, among other fields. 

Both can be linked through the tweet ID.
* The CSV and TSV datasets are provided in two flavors: one with the original 
tweet texts, called   `csv_linebreak` and `tsv_linebreak` respectively; and 
another with newlines replaced by whitespaces, called
  `csv_no_linebreak` and `tsv_no_linebreak` respectively. The latter is 
provided to help participants who may prefer to
  parse these files as plain text, line by line.

## Version list

* __v1.0 [18/01/21]__ Training and development data 

## Contents of the repository

We provide the following files:

* Main folder: [data](data)
  * Subfolder: [data/csv_linebreak](data/csv_linebreak).  <br/>CSV 
(comma-separated values) training and development files with the original tweet 
texts
  * Subfolder: [data/csv_no_linebreak](data/csv__no_linebreak).  <br/>CSV 
(comma-separated values) training and development files with with newlines 
replaced by whitespaces 
  * Subfolder: [data/tsv_linebreak](data/csv_linebreak).  <br/>TSV 
(tab-separated 
values) training and development files with the original tweet texts
  * Subfolder: [data/tsv_no_linebreak](data/tsv_no_linebreak).  <br/>TSV 
(tab-separated values) training and development files with with newlines 
replaced by whitespaces 
  * Subfolder: [data/json](data/json).  <br/>JSON training and development files 
with the objects retrieved from the Twitter API when the tweets were 
downloaded. They contain some additional information (e.g., the class).
* [README.md](README.md) <br/>
  this file

## Data format

The text encoding is UTF-8. The fields included are the following:


* topic_id: unique ID for the topic the tweet is about 
* tweet_id: unique tweet ID (as given by Twitter) 
* tweet_url: URL to the tweet 
* tweet_text: content of the tweet
* claim: 1 if the tweet is a claim; 0 otherwise 
* check-worthiness: 1 if the tweet is worth fact checking; 0 otherwise 

Example:
> politics	1192517071348699136	
https://twitter.com/user/status/1192517071348699136	📅 Mañana, viernes, no 
puedes perderte el gran acto de cierre de campaña en Madrid.   ⏰ A las 19.00 h 
en el Pabellón 1 de IFEMA (Madrid).  Con Kiko Veneno y O'Funk'illo en concierto 
y la intervención de @Pablo_Iglesias_, @AdaColau, @Irene_Montero_, @agarzon...   
¡Te esperamos! https://t.co/IxHyDWdB0S	0	0

Note that the gold labels for the task are the ones in the *check_worthiness* 
column 

## Data Annotation Process


### Evaluation metrics

The official evaluation measure is MAP. 


[CLEF 2021](http://clef2021.clef-initiative.eu/index.php) is the 12th edition of 
the Conference and Labs of the
Evaluation Forum. [CheckThat!](https://sites.google.com/view/clef2021-checkthat) 
is the 4th version of the lab about
Detecting Check-Worthy Claims, Previously Fact-Checked Claims, and Fake News. 
This repository provides the dataset to be
used by participants of **Task 1 - Check-Worthiness Estimation** in Spanish.

