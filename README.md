# BRVB

Matlab code implementing EEG source localization from scalp activity using Variational Bayes (VB):

http://www.scholarpedia.org/article/Source_localization#Sparse_Bayesian_learning_.28SBL.29_and_automatic_relevance_determination_.28ARD.29

Instead of starting from an icosahedron and divide each face until the desired resolution and apply VB on in this last scale, we solve apply VB in multiple scales, using the variance after convergence in each coarse grained scale as prior information to start the next VB better informed in the finer grained scale. 

The goal is to localize the sources in a scale with ~2000 to ~10000 dipoles as usual, but starting from a better starting point compared to constant prior variance accross all dipoles. Usually it need 4 to 5 iterations.

For mor information:

* Backward Renormalization Priors and the Cortical Source Localization Problem with EEG or MEG

http://arxiv.org/abs/1502.03481
