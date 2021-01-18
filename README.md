# CLEF 2021 - CheckThat!

[CLEF 2021](http://clef2021.clef-initiative.eu/index.php) is the 12th edition of the Conference and Labs of the
Evaluation Forum. [CheckThat!](https://sites.google.com/view/clef2021-checkthat) is the 4th version of the lab about
Detecting Check-Worthy Claims, Previously Fact-Checked Claims, and Fake News. This repository provides the dataset to be
used by participants of **Task 1 - Check-Worthiness Estimation** in Spanish.

## The data

* The data consists of tweets from Spanish politicians, annotated by human fact-checkers. Only tweets with a certain
  degree of agreement between fact-checkers were selected.
* We provide a split of the data into train, dev and test sets.
* The train and dev sets are already available for participants. The test set will be released in the future for
  evaluation of the solutions proposed.
* All datasets consist of 3 files: CSV (comma-separated values), TSV (tab-separated values) and JSON. The first two are
  equivalent and contain the tweet text, the tweet ID and the label to be predicted, among other variables. The JSON
  consists of the objects retrieved from the Twitter API when the tweets were downloaded, and contain additional
  information. Both can be linked through the tweet ID.
* Additionally, the CSV and TSV datasets are provided in two flavors: one with the original tweet texts, called
  `csv_linebreak` and `tsv_linebreak` respectively; and another with newlines replaced by whitespaces, called
  `csv_no_linebreak` and `tsv_no_linebreak` respectively. The latter is provided to help participants who may prefer to
  parse these files as plain text, line by line.