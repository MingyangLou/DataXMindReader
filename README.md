# MindReader Data-X
With the goal of better understanding visitor intent on Volvo’s website, six UC Berkeley students created MindReader, a sophisticated mathematical model that defines users’ intentions and types of users. Even though there are some Web Analytics Tools online, ther are no realiable one specifically focusing on implicit intent. MindReader, as the creative solution, uses visitor behavior data to analyze the purchasing intentions behind activities on the website. It innovates in the space of web analytics by applying state-of-the-art machine learning model, Hidden Markov Model, to traditional data science. MindReader identifies the hidden intents of visitors and clusters similar users together to categorize general segements of website visitors. With MindReader, the website managers can better understand their web-visitors and now have the power to personalize their website by targeting on specific user segment to increase overall conversion rates. 

# Methods
At first, we cleaned our millions web data provided from Volvo based on different sessions and split the data into converted user data and non-converted user data. Then, we prepare our data to fit into built-in HMM model in hmmlearn library. We converted continouse observed variable into discrete variable to fit Discrete HMM Model. In our case, hidden states reprent users underlying intents when they stay in different pages of the Website. Then, we decided to choose a large number of states so we can cluster them into communities after. We replaced hidden states with communities for acquiring more abstract factors. So, different types of states are combined into one community. Using networkx, we find the optimal number of communities by optimizing for modularity. Modularity measures the degree to which densely connected compartments within a system can be decoupled into separate communities which interact more among themselves rather than other communities. We output top pages behind each community to define the meaning of the communities. For instance, if a community outputs pages about shopping tools such as ”get local price”, ”request test drive,” and ”submit dealer contract” and exploring Volvo from ”Product detail pages”. We define that users stay in this community when they would like to buy Volvo cars from locals. In the last step, we cluster sessions by creating feature vectors of the porportion of communities in each sequence. We find the optimal number of clusters using the Davies-Bouldin score, which is similar to modularity but used for k-means clustering. It measures the strength and independence of each cluster. From our results table at the end, we have two labelled sessions for converted user data and five labelled sessions for non-converted user data. The Website managers can evaluate specific marketing strategies by targeting on specific user segment.


# Contact us
- **Mike Caballero:** michaelcaballero @ berkeley edu
- **Chenghao Meng:** chm @ berkeley edu
- **Zehao Wei:** zehaowei @ berkeley edu
- **Mingyang Lou:** mingyanglou @ berkeley edu
- **Joo Kim:** jh04023 @ berkeley edu
- **Jaehuk Kim:** kimj98 @ berkeley edu

# License
[Apache2](https://www.apache.org/licenses/LICENSE-2.0)
