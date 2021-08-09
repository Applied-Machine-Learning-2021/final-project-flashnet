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
In this project we want to determine ideal (best) node placement in the Bitcoin Lightning Network so that we may lie on the greatest number of cheapest paths. In order to do so we want to train a model that calculates the betweenness improvement scores of each node and each node's subsequent neighbors and so on and so forth. Our project could then possibly lead to a more viable solution to helping the Lightning Network grow and benefit Bitcoin as a trusted worldwide cryptocurrency. By perfecting the Lightning Network, we can benefit by getting overall lower fees and faster transactions on the main Bitcoin blockchain. This also helps to decrease the average cost of the network.


# Check out the LIVE Lightning Network [here](https://explorer.acinq.co/)!

![image](https://user-images.githubusercontent.com/81460060/128286302-b0f56847-ffc4-44a8-987c-ffdf1043998b.png)


# Process Overview:

## 1. Obtaining our dataset to have our model train on:
We took hourly snapshots of the nodes and edges of the Lightning Network at a given point in time, and filtered out the ones that didn't meet certain criterion (last active, how many connections, satoshis, etc.)

## 2. Making an environment for our model:
We then created an OpenAI gym environment so that our agent could "play on" and train as it "plays the game" or progressively learns.

## 3. Graph Convolutional Network and Deep Graph Library:
GCN and DGL is our model, our model is fed with data from the actor critic.

## 4. ActorCritic:
This is our agent that will perform the act of playing our game. The Actor aspect of the agent makes a decision, and the Critic aspect of the agent determines whether that action was a good one or bad one based on the reward of that action. 

## Usage instructions
<!--
Give details on how to install fork and install your project. You can get all of the python dependencies for your project by typing `pip3 freeze requirements.txt` on the system that runs your project. Add the generated `requirements.txt` to this repo.
-->
*Make sure you have at least 8 GB of RAM in order to run at the minimum 10,000 episodes (iterations/plays of our agent)*

1. Fork this repo
2. Change directories into your project
3. On the command line, type `pip3 install requirements.txt`
4. ....


# Questions? 
Please Feel Free To Contact:
[Vincent Davis](https://github.com/davisv7)

Helpful [forum](https://www.reddit.com/r/TheLightningNetwork/) for any additional questions.

[Start Investing in Bitcoin Now!](https://www.youtube.com/watch?v=dQw4w9WgXcQ)
