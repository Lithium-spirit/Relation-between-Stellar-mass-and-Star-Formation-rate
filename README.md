# Relation-between-Stellar-mass-and-Star-Formation-rate
I have used JWST data to find the relation between SFR and Stellar mass and  converting into parametric relation to measure Cosmological distances for high redshift galaxies . I have checked the redshift dependence of the relation by dividing them into redshift brackets. I have followed the methodology used in https://arxiv.org/pdf/2412.01853
The Code is divided into 5 notebooks. 4 of which are similar code but for different datasets. One notebook is used to plot the results inferred from the first 4 notebooks.
The data is divided as such:
1) z<2.5 this notebook uses the galaxies whose redshift is less than 2.5 from data in li et al
2) z>=2.5 this notebook uses the galaxies with redshift between 2.5=<z<4 from data in li et al
3) MUV<=(-19) this notebook uses galaxies with redshift 5<z<14 from data in morishita et al however it uses galaxies whose MUV<=(-19) to test the dependance of MUV
4) MUV>(-19) this notebook uses galaxies with redshift 5<z<14 from data in morishita et al however it uses galaxies whose MUV>(-19) to test the dependance of MUV
5) Cosmo_Curve uses the parameters inferred from the other notebooks to test the distance modulus and redshift dependance.

For the initial 4 notebooks I have followed the following procedure to infer parameters
1) Data importing.
2) Filtering Data according to requirement.
3) Using linear regression to get approximate initial position for parameters.
4) Using EMCEE module to conduct bayesian analysis Using the prior knowledge obtained from linear regression. We use the likelihood function mentioned in https://arxiv.org/pdf/2412.01853.

Where my results differ from that in the paper is that the parameter values for individual datasets however the final distance modulus and redshift dependance trend appears to be consistent with that in the paper.

Two primary datasets attached here are Li data which is taken from https://iopscience.iop.org/article/10.3847/2041-8213/acf470 however it has been tweaked by me to make it more readable for my code, The other data that is morishita data is taken from https://iopscience.iop.org/article/10.3847/1538-4357/ad1404
