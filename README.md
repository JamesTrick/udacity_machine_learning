# Enron Fraud Udacity Machine Learning Final Project

This repo and markdown is all about identifying Persons of Interest in the Enron scandal of 2001. This project relates to Udacity's Capstone Project for the <a href="https://www.udacity.com/course/intro-to-machine-learning--ud120">ntroduction to Machine Learning Course</a>.

# Pre-requistes/Requirements:

Python 2.7

# Contents

* <a href="https://github.com/JamesTrick/udacity_machine_learning/blob/master/data_exploration.ipynb">data_exploration.ipynb</a> - iPython notebook exploring the Enron data answering Udacity's questions and more
* <a href="https://github.com/JamesTrick/udacity_machine_learning/blob/master/poi_id.py">poi_id.py</a> - Python script with complete machine learning model.

# Background to Enron Scandal

Enron used to be the 7th largest corporation in the United States (US). However, in the late 90s Enron started to experience losses. Instead of reporting these loses, Enron used creative accounting to effectively hide the true financial performance and position of the company. In 2001, Enron filed
for bankruptcy.

The Enron scandal was one of the first major case of corporate mis-management.

## Using machine learning to identify Who's who

The goal of this project and repo is identify persons of interest in the Enron Scandal. To do this, we're going to use Machine Learning techniques implemented in Python. Machine learning is a natural fit for a goal like this as we have large amounts of data, and manually reading, labeling, classifying the data would be prohibitively expensive in terms of labour costs.

# Results
## The Data

In data_exploration.ipynb, we note that we have a dataset comprising of 146 people and their relevant features, eg salary, bonuses, emails, etc.

Exploring this data further, I observed that there was really only on major outlier within the dataset. This outlier was the Total of financial data, simply a result of how the data was initially processed. The results of removing this is displayed below:

I also removed a row of the dataset relating to THE TRAVEL AGENCY IN THE PARK, as the goal of this investigation was to identify persons of interest. Further research into THE TRAVEL AGENCY IN THE PARK found that Sharon Lay, the sister of the then CEO, Kenneth Lay, was the owner of the business and it was found that Enron spent about $5.9m to THE TRAVEL AGENCY IN THE PARK in 2001. While this point is interesting, and likely was used as a way to disperse money, I still decided to remove it from the investigation.

### Feature Creation/Selection

On top of the given features, I created two new features. These aim to represent a relationship between the number of emails sent/received to/from a POI vs the total number of emails sent/received overall. It's represented by the following:

$$ \frac{fromThisPersonToPOI}{fromMessages} $$
$$ \frac{toThisPersonFromPOI}{toMessages} $$

Further processing on this data is simply using the MinMaxScaler from the sklearn package 
# References

### Articles
* <a href="http://www.travelweekly.com/Travel-News/Travel-Agent-Issues/Texas-agency-takes-a-huge-hit-from-Enron-s-fall">Texas agency takes a huge hit from Enron's fall</a>

### Documentation
* Sklearn Documentation (of course!) - http://scikit-learn.org/stable/documentation.html