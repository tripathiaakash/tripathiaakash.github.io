---
layout: post 
title: "System Design for Recommendation Systems - MLOps"
date: 2023-09-09 10:55:40 +0000
category: Recommendation Systems
---

Live Recommendations vs Batch Recommendations - if only 10% of users visit in a day, we are wasting 90% of the compute used during recommendation generation.
Downsides of Live recommendation system:
High Operational Load
API has to be up 24x7
Very Low latency (also high throughput for some cases)
Expensive developer operations and high infrastructure costs

There are two aspects in any live recommendation system:
1. Offline processes: Training, indexing items, building graphs, load data into feature stores
2. Online processes: Use artifacts from the offline processes/environments to serve requests.. In the cases of recommendation systems, the online processes are mainly divided in to two parts: candidate retrieval and ranking

In order for quickly explain these two parts:
1. Candidate Retrieval is generally a service/algorithm that finds X number of nearest neighbouring item vectors given a user vector. This generally happens in a shared latent vector space between users and items. Algorithms such as Collaborative Filtering and Neural Collaborative Filtering (NCF) are some of the common ways to do that. Candidate Retrieval is generally a fast process resulting in a list of matching user-item pairs and the score between them.
2. Ranking is a service which takes user and items from the above and then ranks the items. This process needs to be accurate and hence, more information about the user, the items, and the context is consumed by the ranking algorithm to rank the items.