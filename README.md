# literature-review
Links to papers along with notes.

This is the start of my unofficial blog on recommendations and representation learning.
It might not be the best place to start, but who cares.
I'll (try to) organize the repo by topics for easier referencing.

## Recommendation Systems
1. [Pretrained Transformers for Text Ranking: BERT and beyond](https://arxiv.org/pdf/2010.06467.pdf)

## Ads


## Representation Learning


## Multitask Learning
MMoE


## Other Interesting Topics
### GNN
1. [Introduction to GNN on distil](https://distill.pub/2021/gnn-intro/)
A comprehensive overview of the message-passing-based GNN modeling techniques in 2021.
   - Inductive biases: Problems where the interaction between entities is important will benefit from the graph structure.
   - Choice of aggregation functions: Smooth aggregation function that is invariant to node ordering and the number of nodes.
A desirable property of an aggregation operation is that similar inputs provide similar aggregated outputs, and vice-versa.
   - The mean operation can be useful when nodes have a highly-variable number of neighbors or
  you need a normalized view of the features of a local neighborhood.
   - The max operation can be useful when you want to highlight single salient features in local neighborhoods.
   - Sum provides a balance between these two, by providing a snapshot of the local distribution of features,
  but because it is not normalized, can also highlight outliers. In practice, sum is commonly used.
 
1. [node2vec: Scalable Feature Learning for Graph Networks](https://arxiv.org/pdf/1607.00653.pdf)
The authors propose `node2vec`, a semi-supervised algorithm for scalable feature learning in networks.
They optimize a custom graph-based objective function using SGD motivated by prior work on SkipGram.
Intuitively, their approach returns feature representations that maximize the likelihood of preserving
network neighborhoods of nodes in a d-dimensional feature space.
They use a 2nd order random walk approach to generate (sample) network neighborhoods for nodes.

1. [Semi-Supervised Classification with Graph Convolution Networks](https://arxiv.org/pdf/1609.02907.pdf )
`GCN` is proposed: designs a graph convolutional network via a
localized first-order approximation of spectral graph convolutions.

1. [Inductive Representation Learning on Large Graphs (2018)](https://arxiv.org/pdf/1706.02216.pdf)
`GraphSage` is proposed: define a non-spectral convolution approach that applies
 convolutions directly on the graph, operating on groups of spatially close neighbors.
 Previous to this, most models are transductive (i.e. require all nodes in the graph are present during training
 of the embeddings). `GraphSage` is an inductive framework that leverage node information to efficiently generate 
 embeddings for previously unseen data.
([Link to the code and datasets](http://snap.stanford.edu/graphsage/))

1. [Graph Convolutional Neural Networks for Web-Scale Recommender Systems](https://arxiv.org/pdf/1806.01973.pdf)
`PinSage` is proposed: Similar to `GraphSage`, `PinSage` is an inductive model that compute node embeddings using both
node features as well as topological information. Moreover, (1) the local neiborhood is formed by importance sampling, where
the score of a target node is the normalized visit counts starting from the source node and top T are selected for 
controlling memory footprint and weighted-mean aggregator; (2) sampling is performed on CPU, and batch train the model
on GPU. In addition to the above, the paper also introduces some engineering techniques to ensure efficient training.

### Sequential models
1. [Attention is All You Need](https://arxiv.org/abs/1706.03762)
Learn contextualized token embeddings. Order is introduced via positional encoding.
   - [Illustrated Transformer](https://jalammar.github.io/illustrated-transformer/)
1. 



