Coincidentally as I started working on this assignment, I was assigned a similar assignment in ASM (Applied Statistical Methods). So I am turning in my ASM assignment which penalizes the rank of the latent vector and thereby increasing compression. 

Adding a nuclear normal loss component does not decrease the rank of the latent vector, instead it penalizes large values in the latent vector. As a result, all the values reduce, but the rank remains the same.

On the other hand the majorizer loss does a great job in reducing the rank, although there is a significant variance in compression. The loss used was a log-loss majorizer. 

LoRAE (Low-Rank Autoencoder):
https://arxiv.org/abs/2310.16194
This paper explores the same principles as the assignment, focusing on low-rank latent spaces and compression.


IRMAE (Implicit Rank Minimizing Autoencoder):
Developed by Facebook researchers, this model generalizes the approach used in both the LoRAE and the assignment, offering a broader framework for rank minimization in latent vectors.
https://arxiv.org/abs/2010.00679
