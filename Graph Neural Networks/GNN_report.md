## Graph Neural Networks

I started working on this during my first attempt of the assignment and I found it really interesting. As I was learning more and more about it I noticed a lot of similarities between how social structures influence the characteristics of people and how the message aggregation takes into account the effect of the neighboring nodes. Over time the encodings of each node was influenced by the structure of the data it was surrounded by. 

The basic idea of GNNs which i was quick to grasp was: You update your node encodings based on the current node encoding and the message aggregated from the node’s neighbors. This operation is performed repetitively until a pattern is observed or something could be learned from the final node embeddings. 

Once I familiarized myself with the idea of message aggregation used to update node encodings, I went on to learn about GCNs.

GCNs were pretty simple. In the message aggregation step you normalized the neighboring node features based on the degree of the nodes. Specifically, symmetric normalization is employed; the normalization constant is the square root of the product of the degrees of the source node and the neighbor node. 

This seemed like simple aggregation to me and it made sense. Prioritize inputs from less degree nodes as they provide more information and give less importance to nodes of higher degree as they might not have any specific information helpful for your node. On an intuitive sense this what I understood. 

Thankfully the tutorial on PyG helped understand the implementation of such a layer. 

Now moving to GAT. I found the Antonio Longa tutorial quite helpful in understanding GAT, but and even better resource was the Graph Representation Learning Book. Chapter:5- Graph Neural Network Model, helped me understand GAT really well. 

Essentially we are doing the same thing we did in GCN, but now instead of using symmetric normalizing constants we use attention weights to define a weighted sum of neighbors. The weight denotes the attention on the neighbor and is learned using an MLP, where the first layer consists of the feature vectors of both the source node and the neighbor node and the final layer outputs a single value. Softmax function is used on the output values of the MLP to obtain precise weights of each connection.

I implemented both the GCN and GAT models on the Cora dataset.

