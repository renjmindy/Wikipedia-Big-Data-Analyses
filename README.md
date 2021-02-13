# Wikipedia-Big-Data-Analysis

## Project Description

Project 1's analysis consists of using big data tools to answer questions about datasets from Wikipedia. There are a series of basic analysis questions, answered using Hive or MapReduce. The tool(s) used are determined based on the context for each question. The output of the analysis includes MapReduce jarfiles and/or .hql files so that the analysis is a repeatable process that works on a larger dataset, not just an ad hoc calculation. Assumptions and simplfications are required in order to answer these questions, and the final presentation of results includes a discussion of those assumptions/simplifications and the reasoning behind them. In addition to answers and explanations, this project requires a discussion of any intermediate datasets and the reproduceable process used to construct those datasets. Finally, in addition to code outputs, this project requires a simple slide deck providing an overview of results. The questions follow: 

* Which English wikipedia article got the most traffic on January 20, 2021?
* What English wikipedia article has the largest fraction of its readers follow an internal link to another wikipedia article?
* What series of wikipedia articles, starting with Hotel California, keeps the largest fraction of its readers clicking on internal links? 
* Find an example of an English wikipedia article that is relatively more popular in the Americas than elsewhere. 
* Analyze how many users will see the average vandalized wikipedia page before the offending edit is reversed.
* Run an analysis you find interesting on the wikipedia datasets we're using.

## Technologies Used

* Hadoop MapReduce
* YARN
* HDFS
* Scala 2.13
* Hive
* Git + GitHub

## Features

List of features ready and TODOs for future development
* Join multiple separate data sets 
* Estimate a ratio with the inclusion of codition (or selection criterion) 
* Measure the data size reduction in one given category after applying cuts 

To-do list:
* Take more data over a longer period in order to average out random noises 
* Consider abnormalities in some sub-group of data rather than assuming all behaving uniformly

## Getting Started
   
* Fork this repository.
* Create a branch: git checkout -b <branch_name>.
* Make your changes and commit them: git commit -m '<commit_message>'
* Push to the original branch: git push origin FaceDetectors/<location>
* Create the pull request.

## Usage



## License

This project uses the following license: [<license_name>](<link>).
