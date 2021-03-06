<!--
Name of your teams' final project
-->
# mBIP-BOLT:
## Maximum Betweenness Improvement Problem Basis of Lightning Technology
Node Placement in the Bitcoin Lightning Network

Sponsored by:
## [National Action Council for Minorities in Engineering(NACME)](https://www.nacme.org) Google Applied Machine Learning Intensive (AMLI) at the `UNIVERSITY OF KENTUCKY`

<!--
List all of the members who developed the project and
link to each members respective GitHub profile
-->
Developed by: 
- [Ndizeye Tschesquis](https://github.com/cheskynd) - `Berea College`
- [Renato Diaz](https://github.com/NrgNinja) - `University of Central Florida` 
- [Tony Ramirez](https://github.com/tonypacheco223) - `University of Kentucky` 
- [Daniela Rodriguez](https://github.com/danirodrx) - `Florida International University`
- [Vincent Davis](https://github.com/davisv7) - `University of Kentucky`

# Introducing FlashNet
A service that provides a solution to utilizing the Lightning Network to its utmost potential.

## Description
<!--
Give a short description on what your project accomplishes and what tools is uses. In addition, you can drop screenshots directly into your README file to add them to your README. Take these from your presentations.
-->
A reinforcement agent is used to locate the best node placement in the Bitcoin Lightning Network so that we may lie on the greatest number of cheapest paths. To accomplish this goal a graph convolution network is used to aggregate the features of each node neighbors up to three layers. Open AI gym was the environment for the reinforcement agent, Critical Actor, to interact based on the given inputs. In other words, mBIB-BOLT may lead to a more viable solution to helping the Lightning Network grow and benefit Bitcoin as a trusted worldwide cryptocurrency. By perfecting the Lightning Network, we can benefit by getting overall lower fees and faster transactions on the main Bitcoin blockchain. This also helps to decrease the average cost of the network.


# Check out the LIVE Lightning Network [here](https://explorer.acinq.co/)!

![image](https://user-images.githubusercontent.com/81460060/128286302-b0f56847-ffc4-44a8-987c-ffdf1043998b.png)


# Process Overview:

## 1. Obtaining our dataset to have our model train on:
Three months prior the project, a node was activated in the lightning network and hourly snapshots of the Lightning Network was taken. However, cleaning the data was critical to increase efficiency. The following criteria shows what nodes and edges pass the filter:
|          Node            |        Edges             |
|--------------------------|--------------------------|
|Nodes must been active at least 30 days since the the snapshot was taken |Capacity should be greater than 1,000,000 satoshi|
|Nodes must have a degree greater than two | Must not be dissabled nor have null polices|

The link below contains 100 filter snapshots of the lightning network. To view one file at a time you must download Dadroit json viewer.
https://drive.google.com/file/d/17w4L2yzb2KgSOLRrqQbH84N2UjBytpvu/view?usp=sharing

## 2. Making an environment for our model:
The environment allowed the reinforcement agent to learn from different scenarios and calculate the change of the maximum betweenness centrality for each move made by the agent, which is the reward. As any game, a character has multiple ways to begin a game. In our case, the agent could learn from the entire snapshot which had thousands of nodes. Or a subgraph to maximize the learning rate of the agent. The user can also increase the number of episodes. The more episodes are ran the more the agent will learn from the data. The picture below demonstrates a general idea how the agent interacts with the agent.
![Google AMLI Final Presentation ](https://user-images.githubusercontent.com/81537387/128651863-9dc011a0-d54c-44c4-a3bd-214d83114183.jpg)



## 3. Graph Convolutional Network and Deep Graph Library:
GCN is our model that comes from DGL, a Python package, and allows the program to train on the same agent (the Actor Critic) on varying sizes of graphs. The model is initially fed with four features: betweenness centrality, degree centrality, closeness centrality, and edge vector; and passed into a message passing system that makes up the network of the model to collect feature information about the nodes neighbors. This ends in a resulting feature vector that characterizes the node in context of location and the network to then pass through the GCN for training. It is then aggregated through summation and the output is passed into a linear layer with a 'relu' function.

![Screenshot (138)](https://user-images.githubusercontent.com/81537387/128651754-2fbe82ce-706d-4edd-8c1e-361630c826d0.png)

## 4. ActorCritic:
This is our agent that will perform the act of playing our game. The Actor aspect of the agent makes a decision, and the Critic aspect of the agent determines whether that action was a good one or bad one based on the reward of that action. The critic calculates a TD-Error (Temporal Difference Error), the difference between the expected and acutal reward. The TD-Error is passed to both the actor and critic aspects that helps enables them to learn.
![Google AMLI Final Presentation  (1)](https://user-images.githubusercontent.com/81537387/128651908-5ab9634b-9b30-42ec-8b80-17970b93b037.jpg)


## Usage instructions
<!--
Give details on how to install fork and install your project. You can get all of the python dependencies for your project by typing `pip3 freeze requirements.txt` on the system that runs your project. Add the generated `requirements.txt` to this repo.
-->
*Make sure you have at least 8 GB of RAM in order to run at the minimum 10,000 episodes (iterations/plays of our agent)*

1. Fork this repo
2. Change directories into your project
3. Download the snapshot zipfile and place it in your repo.
4. Change manually in the main.py on how to interact with the enviroment.
   * Snapshot vs. Subgraph 
   * Number of episodes 
   * Node ID (Already existing node in the network) else None (New node)
   * load_model (reload the model)
   * Budget (How many nodes to add to the node to maximize its betweeness centrality)
5. run the program 'python3 main.py'
6. Analyze the results
# Questions? 
Please Feel Free To Contact:
- [Vincent Davis](https://github.com/davisv7)
- Tony Ramirez : tpra223@uky.edu 
- Ndizeye Tschesquis : tschesquisn@berea.edu
- Renato Diaz: diazrenato2001@outlook.com

Helpful [forum](https://www.reddit.com/r/TheLightningNetwork/) for any additional questions.

[Start Investing in Bitcoin Now!](https://www.youtube.com/watch?v=dQw4w9WgXcQ)
