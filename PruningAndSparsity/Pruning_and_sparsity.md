# Pruning and Sparsity

For this problem I implemented VGG16. It comfortably met the criteria of model size being greater than 35 MB, in fact my model size came out to be 128 MB. The thing I struggled with most in this project was getting the accuracy to be greater than 90 percent, I ended up with an 83 percent accuracy.

After implementation of the model I could go ahead with plotting the weight distribution of each of the layers. As predicted from the lectures most of my weights were zeroes. In the sensitivity scan I plotted my accuracy values from sparsities 0 to 1 with a step size of 0.1.  From the sensitivity scan I selected the sparsity values for which the accuracy dropped the least. I fixed those sparsity values and fine pruned the model. This dropped the accuracy to 42 percent and reduced the model size by 50 percent. 

After fine tuning the model accuracy reached 84 percent which is better than the pre-pruned accuracy of the model - 82.64 percent.
