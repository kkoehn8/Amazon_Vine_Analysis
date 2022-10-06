# Amazon_Vine_Analysis

## Overview of the analysis
For this project we are analyzing reviews written by members of the Amazon Vine program. After the initial analysis we are determining if there is any positivity bias for the reviews in the Vine program.

The tools used for this project are:
 - AWS database
 - Postgres database
 - Google Colab notebook

The data was obtained from the following location: https://s3.amazonaws.com/amazon-reviews-pds/tsv/index.txt and for this specific analysis I analyzed the Outdoors US dataset. 

Once the data was imported from an AWS database into our Postgres database we exported the Vine review data for additional analysis. An analysis of the Vine data was conducted to determine if participants in the Vine program were more likely to provide 5 star reviews than non-participants.

## Results
Initially we retrieved items with 20 or more total votes and that data was further reduced to items where the number of helpful votes divided by the total votes was greater than or equal to 50%. The image below shows the first 20 rows of the data that met the above criteria.

![Vine_Reviews](https://github.com/kkoehn8/Amazon_Vine_Analysis/blob/main/Images/Vine_Reviews.PNG)

The data was then subsetted based on if the review was a Vine Review or not the the results are shown below. 

Vine Reviews:
 - Total Reviews: 107
 - 5 Star Reviews: 56
 - Percentage of 5 Star Reviews: 52.3%

Non Vine Reviews:
 - Total Reviews: 39,869
 - 5 Star Reviews: 21,005
 - Percentage of 5 Star Reviews: 52.7%

## Summary: 
After reviewing the results of the analysis there appears to be no difference in positivity bias between Vine reviews and Non Vine reviews. Additionally, for the Outdoor data, the percentage of 5 Star Reviews for Non Vine members, at 52.7%, is actually 0.5% higher than for Vine members. 

The data does show that there is a much greater number of Non Vine reviews (39,869) to Vine reviews (107). 

Using the same dataset we can determine the mean number of stars ratings for both Vine members and Non Vine members to determine if there are additional differences or if the reviews are very similar regardless if the reviewer is a Vine member or Non Vine member. 

