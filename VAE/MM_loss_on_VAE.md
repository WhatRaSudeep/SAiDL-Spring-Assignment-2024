Coincidentally as I started working on this assignment, I was assigned a similar assignment in ASM (Applied Statistical Methods). So I am turning in my ASM assignment which penalizes the rank of the latent vector and thereby increasing compression. 

Adding a nuclear normal loss component does not decrease the rank of the latent vector, instead it penalizes large values in the latent vector. As a result, all the values reduce, but the rank remains the same.

On the other hand the majorizer loss does a great job in reducing the rank, although there is a significant variance in compression. The loss used was a log-loss majorizer. 

LoRAE (Low-Rank Autoencoder):

[https://arxiv.org/abs/2310.16194#:~:text=24 Oct 2023]-,Learning Low-Rank Latent Spaces with Simple,Autoencoder%3A Theoretical and Empirical Insights&text=The autoencoder is an unsupervised,by minimizing the reconstruction loss]
The above paper implements the same idea as the assignment. 

IRMAE (Implicit Rank Minimizing Autoencoder):

This idea came up by facebook researchers and implements a more generalized version of what was accomplished in the LoRAE and the assign

https://arxiv.org/abs/2010.00679
