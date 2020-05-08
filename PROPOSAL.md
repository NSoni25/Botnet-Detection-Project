                                                      Data Science COMP6200
                                                 Data Science Project Proposal
                                       Topic Name: Botnet Detection using Machine Learning
Summary:

The increasing reliance on the Internet in our daily lives adds a lot of challenges in terms of managing the Internet and the application usage, such as protecting the user data, privacy, integrity and availability. In couple of years, the Internet will play an important role in our lives, especially in communication, education, government services, banking, and e-commerce. Unfortunately, the increasing demands on the user applications has become a threat to his privacy and data security.
A botnet is a logical collection of internet-connected devices such as computers, smartphones or IoT devices whose security has been breached and control ceded to a third party. Each such compromised device, known as a "bot", is created when a device is penetrated by software from a malware (malicious software) distribution. The controller of a botnet is able to direct the activities of these compromised computers through communication channels formed by standards-based network protocols such as IRC and Hypertext Transfer Protocol (HTTP).

Aim/ Goal:

our main goal is to identify if the packet of the network most probably from bot or not and to find out which is the most important factor in this. Our focus is to work on the mentioned research paper: https://ieeexplore.ieee.org/document/7847158

Description/ Approach:

There are mainly two approaches for botnet detection and tracking. One approach is based on setting up honeynets, which is mostly useful to understand botnet technology and characteristics but does not necessarily detect bot infection. The other approach for botnet detection is based on passive network traffic monitoring and analysis. 
ZeZeus, ZeuS, or Zbot is a Trojan horse malware package that runs on versions of Microsoft Windows. While it can be used to carry out many malicious and criminal tasks, it is often used to steal banking information by man-in-the-browser keystroke logging and form grabbing. It is also used to install the Crypto Locker ransomware. Zeus is spread mainly through drive-by downloads and phishing schemes.
The basic idea is to extract feature information on the packets from the traffic and march the patterns registered in the knowledge base of existing bots.

Dataset : 

we are expecting to collect the dataset by using Zeus botnet toolkit into one machine and using the other machine to collect the network traffic. We are planning to implement, CONIFA, and the standard machine learning framework used by researchers in the literature in where they should contain both botnet and non-botnet network traffic. For botnet network traffic representation, Zeus will be considered as, it is one of the major threats, especially for online bank attacks. As the main goal of this experiment is to address the ability to detect the untrained version. For this experiment, we are focusing on collecting only the HTTP GET connection to increase the chances to identify the infected device before uploading/stealing any data from it.
The afore mentioned sources ensure the variety of the collected HTTP network traffic in which they replicate the use of the internet in the real-life scenarios by different users. To build a classifier to detect botnet C&C traffic using the standard framework used by researchers, statistical features should first be identified. After that we are expecting to used Wireshark to detect statistical features from the data.

Techniques used: 

Our aim is to implement exploratory data analysis and descriptive statistical techniques to learn more about the data , since this project is similar to the literature provided above we might be working on inferential statistics techniques to make a model which can be used on any datasets.
we are hoping to work on decision trees, random forest, and other known algorithms to work on this. we are expecting to check which algorithm will be best case scenarios in working on it. 
Since this is more of a classifying problem, so we might be focussing more toward classifying the data and working on it we are more inclined toward working on decision trees.

Advantages of using a Decision tree as classifiers: -

1.It is simple to understand and can be interpreted easily
2.It required little data preparation.
3.The cost of using the tree (i.e., predicting data) is logarithmic in the number of data points used to train the tree.

Disadvantage 

1.Decision-tree learners can create over-complex trees that do not generalise the data well. This is called overfitting
2.Decision tree learners create biased trees if some classes dominate. It is therefore recommended to balance the dataset prior to fitting with   the decision tree.

K-10 cross validation

Cross-validation, sometimes called rotation estimation, or out-of-sample testing is any of various similar model validation techniques for assessing how the results of a statistical analysis will generalize to an independent data set. The goal of cross-validation is to test the model’s ability to predict new data that was not used in estimating it, in order to flag problems like overfitting or selection bias and to give an insight on how the model will generalize to an independent dataset (i.e., an unknown dataset, for instance from a real problem).
Project Plan:

Week 10: Data Collecting   and wrangling

1.      Discovering
2.      Structuring
3.      Cleaning
4.      Enriching
5.      Validating
6.      Publishing

Week 11: Applying Data Analysis techniques

1. Descriptive Analysis
2. inferential Analysis
3. Regression/classification Analysis 
4. Fuzzy Logic
5. Decision Trees

Week 12:

Visualization and Presentation Preparation
