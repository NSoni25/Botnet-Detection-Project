                                                   Data Science COMP6200
                                                Data Science Project Proposal
Topic Name: Botnet Detection using Machine Learning

Summary:

The increasing reliance on the Internet in our daily lives adds a lot of challenges in terms of managing the Internet and the application usage, such as protecting the user data, privacy, integrity and availability. In couple of years, the Internet will play an important role in our lives, especially in communication, education, government services, banking and e-commerce. Unfortunately, the increasing demands on the user applications has become a threat to his privacy and data security.

 Based on McAfee Labs statistics, the number of newly discovered malware samples has reached 50 millions in the fourth quarter of 2014 and expected to reach half a billion by the end of 2015. Moreover, the Internet trafﬁc consisted of up to 80 % of botnets trafﬁc related to spam e-mails originating from known botnets such as Grum, Cutwail and Rustock. Currently, a large scale of botnets can be more than one million PCs launching cyber attacks.A botnet is a logical collection of internet-connected devices such as computers, smartphones or IoT devices whose security has been breached and control ceded to a third party. Each such compromised device, known as a "bot", is created when a device is penetrated by software from a malware (malicious software) distribution. The controller of a botnet is able to direct the activities of these compromised computers through communication channels formed by standards-based network protocols such as IRC and Hypertext Transfer Protocol (HTTP).
Botnets are increasingly rented out by cyber criminals as commodities for a variety of purposes.


Aim/ Goal:

our main goal is to identify if the packet of the network most probably from bot or not  and to find out which is the most important factor in this. Our main focus is to work on this Researach paper : https://ieeexplore.ieee.org/document/7847158



Description/ Approach:

There are mainly two approaches for botnet detection and tracking . One approach is based on setting up honeynets, which is mostly useful to understand botnet technology and characteristics, but does not necessarily detect bot infection. The other approach for botnet detection is based on passive network traffic monitoring and analysis. Botnet detection techniques based on passive traffic monitoring have been useful to identify the existence of botnets. Based on detection method, these techniques can be classified as being signature-based and anomaly-based. Another classification based on audit source location can categorize these techniques into host-based and network-based.
Honeypot refers to a decoy system to entice the attention of attackers to attack this computer system to having an aim of protecting the critical targets . 
This technique is very effective for gathering compact high value information such as signature of bots for content-based detection, information of botnet C&C mechanism/servers, unknown security holes that enable bots to penetrate the network.
The system adjusts to changes in the organizational network based on the dynamic deployment and configuration of low-interaction honeypots (honeyds). 
The main idea is for the honeyds to be deployed using available unused IP addresses such that the distribution of operating, systems and services they emulate mimics that of the operating systems and services of the production hosts in the network. 

The basic idea is to extract feature information on the packets from the traffic and march the patterns registered in the knowledge base of existing bots . Apparently, it is easy to carry on by simply comparing every byte in the packet, but it also goes with several drawbacks . Firstly, it is unable to identify the undefined bots. Second, it should always update the knowledge base with new signatures, which enhances the management cost and reduces the performance. Third, new bots may launch attacks before the knowledge base are patched. 

 Based on detection method, these techniques can be classified as being signature-based and anomaly-based. 
1) Signature-based Detection
2) Anomaly-based Detection

 A packet decoder captures packets from network interfaces and setup the packets to be preprocessed or to be sent to the detection engine. A preprocessor captures the raw packet and check them against certain plugins. These plugins check for a certain type of behavior from the packets. The preprocessor detects anomalies in packet headers and then generate alerts. Once packets have been handled by all enabled preprocessors, they are handed off to the detection engine to be checked through a set of rules. 

Anomaly-based detection techniques attempt to detect botnets based on several network traffic anomalies such as high network latency, high volumes of traffic, traffic on unusual ports, and unusual system behavior that could indicate presence of malicious bots in the network .

Host-based systems focus on detecting bot infections on an individual host and typically use signature- or behavior-based methods to correlate network traffic or system events with known bot signatures or behavioral information [50]. While host-based techniques are able to detect single bot infections, some knowledge of the bots behavior must be known in advance. Host-based approaches also benefit from being easy to deploy and from empowering the end-user directly.
 
Network-based methods attempt to detect bot infections by correlating similar behaviors among several different hosts on the monitored network. Network-based methods do not need prior knowledge of bot signatures or behavioral information as they rely on the intuition that hosts infected by the same bot will behave very similarly to one another whereas uninfected hosts will exhibit different network characteristics from one another . 
While network-based detection systems may not require prior knowledge of a bot’s behavioral patterns, they do require that multiple hosts in the same network become infected for the intrusion to be detectable. In addition, network-based approaches may require additional cooperation of the network administrator and care must be taken to protect the privacy of the network users .


ZeZeus, ZeuS, or Zbot is a Trojan horse malware package that runs on versions of Microsoft Windows. While it can be used to carry out many malicious and criminal tasks, it is often used to steal banking information by man-in-the-browser keystroke logging and form grabbing. It is also used to install the CryptoLocker ransomware.Zeus is spread mainly through drive-by downloads and phishing schemes. First identified in July 2007 when it was used to steal information from the United States Department of Transportation, it became more widespread in March 2009. In June 2009 security company Prevx discovered that Zeus had compromised over 74,000 FTP accounts on websites of such companies as the Bank of America, NASA, Monster.com, ABC, Oracle, Play.com, Cisco, Amazon, and BusinessWeek. Similarly to Koobface, Zeus has also been used to trick victims of technical support scams into giving the scam artists money through pop-up messages that claim the user has a virus, when in reality they might have no viruses at all. The scammers may use programs such as Command prompt or Event viewer to make the user believe that their computer is infected.


Command and control or C2 is a "set of organizational and technical attributes and processes that employs human, physical, and information resources to solve problems and accomplish missions" to achieve the goals of an organization or enterprise, according to a 2015 definition by military scientists Marius Vassiliou, David S. Alberts and Jonathan R. Agre,The term often refers to a military system.

Versions of the United States Army Field Manual 3-0 circulated circa 1999, define C2 in a military organization as the exercise of authority and direction by a properly designated commanding officer over assigned and attached forces in the accomplishment of a mission.

A 1988 NATO definition, command and control is the exercise of authority and direction by a properly designated individual over assigned resources in the accomplishment of a common goal. An Australian Defence Force definition, similar to that of NATO, emphasises that C2 is the system empowering designated personnel to exercise lawful authority and direction over assigned forces for the accomplishment of missions and tasks.(The Australian doctrine goes on to state: The use of agreed terminology and definitions is fundamental to any C2 system and the development of joint doctrine and procedures. The definitions in the following paragraphs have some agreement internationally, although not every potential ally will use the terms with exactly the same meaning.)

 Dataset : 
 we are  expecting to collect the dataset by using zeus botnet toolkit into one machine and using the other machine to collect  the network traffic . We are planning to implement , CONIFA, and the standard machine learning framework used by researchers in the literature in where they should contain both botnet and non-botnet network traffic.For botnet network traffic representation, Zeus will be considered as , it is one of the major threats, especially for online bank attacks. As the main goal of this experiment is to address the ability to detect the untrained version. For this experiment, we are focusiing on collecting  only the HTTP GET connection to increase the chances to identify the infected device before uploading/stealing any data from it.

The aforementioned sources ensure the variety of the collected HTTP network traffic in which they replicate the use of the internet in the real life scenarios by different users.In order to build a classifier to detect botnet C&C traffic using the standard framework used by researchers,  statistical features should first be identified. The mining of statistical features is conducted by applying deep analysis for the collected network traffic.  Tools such as Wireshark will be  used to help  us extract and identify different features of the collected network traffic. The analysis will be  conducted by monitoring the C&C packets behaviour over time within a flow as well as checking the header’s values, and extracted features that express their behaviour and help in distinguishing them from the benign flows.


Techniques used: 
Our aim is to implement exploratory data analysis and descriptive stastical techniques to learn more about the data , since this project is similiar to the literature provided above we might be working on inferential stastics techniques to make a model which can be used on any datasets.

we are hoping to work on decission trees , random forest and other known algorithms to work on this. we are expecting to check which algorithm will be best case scenarios in working on it. 

Since this is more of a classiying problem , so we might be focussing more toward classifying the data and working on it  we are more inclined toward working on decission trees.

Decision Trees (DTs) 
Decision Tree Classifier, repetitively divides the working area(plot) into sub part by identifying lines. 
Decision tree classifiers:
Decision Tree Classifier, repetitively divides the working area(plot) into sub part by identifying lines. 

Advantages of Decision tree classifiers

Simple to understand and to interpret. Trees can be visualised.
Requires little data preparation. Other techniques often require data normalisation, dummy variables need to be created and blank values to be removed. Note however that this module does not support missing values.
The cost of using the tree (i.e., predicting data) is logarithmic in the number of data points used to train the tree.
Able to handle both numerical and categorical data. Other techniques are usually specialised in analysing datasets that have only one type of variable. See algorithms for more information.
Able to handle multi-output problems.
Uses a white box model. If a given situation is observable in a model, the explanation for the condition is easily explained by boolean logic. By contrast, in a black box model (e.g., in an artificial neural network), results may be more difficult to interpret.
Possible to validate a model using statistical tests. That makes it possible to account for the reliability of the model.
Performs well even if its assumptions are somewhat violated by the true model from which the data were generated.


Disadvantage 

Decision-tree learners can create over-complex trees that do not generalise the data well. This is called overfitting. Mechanisms such as pruning (not currently supported), setting the minimum number of samples required at a leaf node or setting the maximum depth of the tree are necessary to avoid this problem.
Decision trees can be unstable because small variations in the data might result in a completely different tree being generated. This problem is mitigated by using decision trees within an ensemble.
The problem of learning an optimal decision tree is known to be NP-complete under several aspects of optimality and even for simple concepts. Consequently, practical decision-tree learning algorithms are based on heuristic algorithms such as the greedy algorithm where locally optimal decisions are made at each node. Such algorithms cannot guarantee to return the globally optimal decision tree. This can be mitigated by training multiple trees in an ensemble learner, where the features and samples are randomly sampled with replacement.
There are concepts that are hard to learn because decision trees do not express them easily, such as XOR, parity or multiplexer problems.
Decision tree learners create biased trees if some classes dominate. It is therefore recommended to balance the dataset prior to fitting with the decision tree.


K-10 cross validation 

Cross-validation, sometimes called rotation estimation,or out-of-sample testing is any of various similar model validation techniques for assessing how the results of a statistical analysis will generalize to an independent data set. It is mainly used in settings where the goal is prediction, and one wants to estimate how accurately a predictive model will perform in practice. In a prediction problem, a model is usually given a dataset of known data on which training is run (training dataset), and a dataset of unknown data (or first seen data) against which the model is tested (called the validation dataset or testing set). The goal of cross-validation is to test the model’s ability to predict new data that was not used in estimating it, in order to flag problems like overfitting or selection bias and to give an insight on how the model will generalize to an independent dataset (i.e., an unknown dataset, for instance from a real problem).




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

Week 12: Visualization and Presetation Preparation
