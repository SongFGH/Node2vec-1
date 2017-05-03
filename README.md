# Firas_BEN-HASSAN

This repository provides a reference implementation of node2vec as described in the paper:


The node2vec algorithm learns continuous representations for nodes in any (un)directed, (un)weighted graph. 

CORA ML Dataset
The Cora dataset consists of Machine Learning papers.
 These papers are classified into one of the following seven classes:
  Case_Based
  Genetic_Algorithms 
 Neural_Networks 
 Probabilistic_Methods
 Reinforcement_Learning 
 Rule_Learning 
 Theory

Basic Usage

Example

To run node2vec on cora network, execute the following command from the project home directory:
python src/main.py --input graph/cora.edgelist --output emb/cora.emd

Options

You can check out the other options available to use with node2vec using:
python src/main.py --help

Input

The supported input format is an edgelist:

node1_id_int node2_id_int <weight_float, optional>
The graph is assumed to be undirected and unweighted by default. These options can be changed by setting the appropriate flags.

Output

The output file has n+1 lines for a graph with n vertices. The first line has the following format:

num_of_nodes dim_of_representation
The next n lines are as follows:

node_id dim1 dim2 ... dimd
where dim1, ... , dimd is the d-dimensional representation learned by node2vec.
