# Capstone: Market Basket Analysis
Capstone Project at the General Assembly, 2021

**Table of Contents**

**Problem Statement**

Analyze Instacart dataset and determine market basket mix based on previous customer order history. 

**Executive Summary**

In this work, I analyze Instacart orders dataset to make predictions about future customer purchases.

**Background Research**



**Model Details**

FP-Growth (Frequent Pattern) is a significantly more efficient algorithm compared to Apriori as the dataset does not need to be scanned over and over again and no candidate generation is required. It scans the dataset and counts frequencies of each item in a dataset, sorting them in descending order and leaving items that are at or above a state support level. The algorithm then loops through the remaining itemsets to build FP-tree of nodes starting from the root - the most frequent occurring item - then the next until it reaches the least represented item in a dataset. When items are not part of the branch, a new branch will be created. The algorithm employs a recursive divide-and-conquer approach to identify frequent itemsets traversing the FP-tree. 

Having done these two steps of data sorting, the algorithm scans for itemsets with support level at least the specified level (e.g. 1000). The FP-trees are built in a way that the root of a tree is conditional upon an item and recursively counts the frequency of the item spotted in an itemset. It works based on a notion that If an item occurs frequently, then a subset(s) of that item should also occur frequently. 

**Visual Representation of the FP-Growth Algorithm**

**Key Findings and Recommendations**

**File Directory**

**Data Dictionary**

**Citations**
See sources.md