# Wikipedia-Big-Data-Analysis

## Project Description

Project 1's analysis consists of using big data tools to answer questions about datasets from Wikipedia. There are a series of basic analysis questions, answered using Hive or MapReduce. The tool(s) used are determined based on the context for each question. The output of the analysis includes MapReduce jarfiles and/or .hql files so that the analysis is a repeatable process that works on a larger dataset, not just an ad hoc calculation. Assumptions and simplfications are required in order to answer these questions, and the final presentation of results includes a discussion of those assumptions/simplifications and the reasoning behind them. In addition to answers and explanations, this project requires a discussion of any intermediate datasets and the reproduceable process used to construct those datasets. Finally, in addition to code outputs, this project requires a simple slide deck providing an overview of results. The questions follow: 

      Q1: Which English wikipedia article got the most traffic on January 20, 2021?
      Q2: What English wikipedia article has the largest fraction of its readers follow an internal link to another wikipedia article?
      Q3: What series of wikipedia articles, starting with Hotel California, keeps the largest fraction of its readers clicking on internal links? 
      Q4: Find an example of an English wikipedia article that is relatively more popular in the Americas than elsewhere. 
      Q5: Analyze how many users will see the average vandalized wikipedia page before the offending edit is reversed.
      Q6: Run an analysis you find interesting on the wikipedia datasets we're using.

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
![Fig.1](https://github.com/renjmindy/Wikipedia-Big-Data-Analysis/blob/main/pic/pj1-wb-2.png)
* Consider abnormalities as appeared in some sub-groups of data rather than assuming all behaving uniformly
![Fig.2](https://github.com/renjmindy/Wikipedia-Big-Data-Analysis/blob/main/pic/pj1-wb-3.png)

## Links for data

* [Pageviews Filtered to Human Traffic](https://wikitech.wikimedia.org/wiki/Analytics/Data_Lake/Traffic/Pageviews)
* [Page Revision and User History](https://wikitech.wikimedia.org/wiki/Analytics/Data_Lake/Edits/Mediawiki_history_dumps#Technical_Documentation)
* [Monthly Clickstream](https://meta.wikimedia.org/wiki/Research:Wikipedia_clickstream)

## Getting started

* Download + install Hive

   - cd to your home directory
         
         - wget https://mirrors.sonic.net/apache/hive/hive-2.3.8/apache-hive-2.3.8-bin.tar.gz
   
   - wait for this complete
         
         - tar -xvzf apache-hive-2.3.8-bin.tar.gz
         
* Add exports to .bashrc

         - sudo nano .bashrc

   - Add the lines below to the .bashrc that opens, replacing username with your username

         - export HADOOP_HOME=/home/username/hadoop-2.7.7
         - export HIVE_HOME=/home/username/apache-hive-2.3.8-bin
         - export PATH=$HADOOP_HOME/bin:$HIVE_HOME/bin:$PATH

   - Additional shortcuts, from Danny:

         - alias startdfs='$HADOOP_HOME/sbin/start-dfs.sh'
         - alias startyarn='$HADOOP_HOME/sbin/start-yarn.sh'
         - alias stopdfs='$HADOOP_HOME/sbin/stop-dfs.sh'
         - alias stopyarn='$HADOOP_HOME/sbin/stop-yarn.sh'

   - Close and restart your Ubuntu shell.

## Contributing to Wikipedia Big Data Analysis
   
* Fork this repository.
* Create a branch: git checkout -b <branch_name>.
* Make your changes and commit them: git commit -m '<commit_message>'
* Push to the original branch: git push origin Wikipedia-Big-Data-Analysis/<location>
* Create the pull request.

Alternatively see the GitHub documentation on [creating a pull request](https://help.github.com/en/github/collaborating-with-issues-and-pull-requests/creating-a-pull-request).

## HQL Source Codes For Each Question Study

* **Top10** articles which attract most views
[Q1](https://github.com/renjmindy/210104-usf-bigdata/blob/main/proj1_0/Project1Q1.sql)/[A1](https://github.com/renjmindy/210104-usf-bigdata/blob/main/proj1_0/Q1A/p1q1t1.tsv)
* **Top10** articles (grouped by subjects/titles) which attract most overall views
[Q1+](https://github.com/renjmindy/210104-usf-bigdata/blob/main/proj1_0/Project1Q1%2B.sql)/[A1v1](https://github.com/renjmindy/210104-usf-bigdata/blob/main/proj1_0/Q1A%2B/p1q9t1.tsv)/[A1v2](https://github.com/renjmindy/210104-usf-bigdata/blob/main/proj1_0/Q1A%2B/p1q9t2.tsv)
* **Top600** subjects/titles which attract most click counts via internal link only, given three types of links: internal, external and others
[Q2](https://github.com/renjmindy/210104-usf-bigdata/blob/main/proj1_0/Project1Q2.sql)/[A2](https://github.com/renjmindy/210104-usf-bigdata/blob/main/proj1_0/Q2A/p1q2t2_8.tsv)
* **Top600** subjects/titles which attract most views from readers via clicking on internal link only
[Q2+](https://github.com/renjmindy/210104-usf-bigdata/blob/main/proj1_0/Project1Q2%2B.sql)/[A2](https://github.com/renjmindy/210104-usf-bigdata/blob/main/proj1_0/Q2A%2B/p1q7t5_1.tsv)
* **Top600** articles which starts with "Hotel_California" attract most click counts via internal link only 
[Q3](https://github.com/renjmindy/210104-usf-bigdata/blob/main/proj1_0/Project1Q3.sql)/[A3](https://github.com/renjmindy/210104-usf-bigdata/blob/main/proj1_0/Q3A/p1q3t1_3.tsv)
* **Top600** articles which starts with "Hotel_California" attract most views from readers via clicking on internal link only
[Q3+](https://github.com/renjmindy/210104-usf-bigdata/blob/main/proj1_0/Project1Q3%2B.sql)/[A3](https://github.com/renjmindy/210104-usf-bigdata/blob/main/proj1_0/Q3A%2B/p1q8t7_1.tsv)
* **Top100** articles which attract most views in America than anywhere else
[Q4](https://github.com/renjmindy/210104-usf-bigdata/blob/main/proj1_0/Project1Q4.sql)/[A4(1)](https://github.com/renjmindy/210104-usf-bigdata/blob/main/proj1_0/Q4A/p1q4t1_d201229_00_05.tsv)/[A4(2)](https://github.com/renjmindy/210104-usf-bigdata/blob/main/proj1_0/Q4A/p1q4t1_d201229_06_11.tsv)/[A4(3)](https://github.com/renjmindy/210104-usf-bigdata/blob/main/proj1_0/Q4A/p1q4t1_d201229_12_17.tsv)/[A4(4)](https://github.com/renjmindy/210104-usf-bigdata/blob/main/proj1_0/Q4A/p1q4t1_d201229_18_23.tsv)
* **Top600** articles which attract most views in America than anywhere else 
[Q4+](https://github.com/renjmindy/210104-usf-bigdata/blob/main/proj1_0/Project1Q4v2.sql)/[A4(1)](https://github.com/renjmindy/210104-usf-bigdata/blob/main/proj1_0/Q4A/p1q4t1_d201229_00_05_2.tsv)/[A4(2)](https://github.com/renjmindy/210104-usf-bigdata/blob/main/proj1_0/Q4A/p1q4t1_d201229_06_11_2.tsv)/[A4(3)](https://github.com/renjmindy/210104-usf-bigdata/blob/main/proj1_0/Q4A/p1q4t1_d201229_12_17_2.tsv)/[A4(4)](https://github.com/renjmindy/210104-usf-bigdata/blob/main/proj1_0/Q4A/p1q4t1_d201229_18_23_2.tsv)
* **Top600** ratios of users to revision counts for all pages
[Q5](https://github.com/renjmindy/210104-usf-bigdata/blob/main/proj1_0/Project1Q5.sql)/[A5](https://github.com/renjmindy/210104-usf-bigdata/blob/main/proj1_0/Q5A/p1q5t1_3.tsv)
* **Top600** average ratios of users to revision counts for one given page: taking average over all correpsonding ratios of user numbers to revision counts to all pages
[Q5+](https://github.com/renjmindy/210104-usf-bigdata/blob/main/proj1_0/Project1Q5v2.sql)/[A5](https://github.com/renjmindy/210104-usf-bigdata/blob/main/proj1_0/Q5A/p1q5t4_1.tsv)
* Measure data size reduction after taking the reversion of offending edits into consideration
[Q6](https://github.com/renjmindy/210104-usf-bigdata/blob/main/proj1_0/Project1Q6.sql)/[A6](https://github.com/renjmindy/210104-usf-bigdata/tree/main/proj1_0/Q6A)

## License

This project uses the following license: [MITlicense](https://mit-license.org/).
