# NSC
A Nulling Self Calibration data reduction program.

The Simon_NSC file tries to improve the NSC algorithm in comparisson to already existing ones (_Making high-accuracy null depth
measurements for the LBTI exozodi survey_, _Nulling data reduction and on-sky performance of the large binocular telescope_). It does this by working with an analytical description of the probability density function of the data. The file is self-explanatory and tries to show the entire tought process. 

The best way to improve this method is by speeding up the evaluation time of Int_func(). This is the function that will be evaluated during the MCMC, and will thus be the bottleneck of our speed capabilities. An other great improvement would be to work directily in a bayesian programming package i.e. STAN, pymc3,... and work directly on the data without having to bin it first. 
