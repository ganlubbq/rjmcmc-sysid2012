rj-mcmc-std
===========

Reversible-Jump Markov Chain Monte Carlo sampler for inference in ARX models with Student-t innovations

This code was downloaded from < https://github.com/compops/rj-mcmc-std > or from < http://www.rt.isy.liu.se/~johda87/code.html > and contains the code used to produce the results in 

J. Dahlin, F. Lindsten, T. B. Schön and A. Wills, 
Hierarchical Bayesian ARX models for robust inference. 
The 16th IFAC Symposium on System Identification, Brussels, Belgium, 2012.

which is available as a draft from < http://www.rt.isy.liu.se/~johda87/publications.html >.

------------------------------
-- Included files           --
------------------------------

RUNME_simulationstudy
The code reproduces the comparision presented in Section 5.1. Note that the
results from that section is based on 25 000 randomly generated systems and 
the provided code only simulates 100 systems. 

RUNME_EEG
The code reproduces a similar output as presented in Fig 3 of Section 5.3.
Using real EEG data, kindly provided by Eline Borch Petersen and Thomas Lunner
at Eriksholm Research Centre, Oticon A/S, Denmark.

Helpfiles and subroutines are found in the folder "helpers":
buildPhi/buildY:       builds the Phi and Y matrix containing the values of u and y.
dexprnd:               generates a discrete exponentially distributed random number
genrndARXmodel:        generates random ARX models with Gaussian/Student's t-noise, outliers and missing data. 
                       (note that this function is not perfect and may sometimes generate strange ARX systems)
igamrnd:               generates inverse gamma distributed random variables
method_createdatasets: divides the output from the random ARX generation function into estimation and validation data.
method_validate:       validates the model and calculates the performance measures (RMSE and VAF)
