# s17lc  (as revised by ksl)

This is a repository for the radio light curve program used in [Sarbadhicary et al 2017](http://adsabs.harvard.edu/abs/2017MNRAS.464.2326S). **Please cite the paper if you use the code for your project**. Here is the BibteX citation:
```@ARTICLE{2017MNRAS.464.2326S,
   author = {{Sarbadhicary}, S.~K. and {Badenes}, C. and {Chomiuk}, L. and 
	{Caprioli}, D. and {Huizenga}, D.},
    title = "{Supernova remnants in the Local Group - I. A model for the radio luminosity function and visibility times of supernova remnants}",
  journal = {\mnras},
archivePrefix = "arXiv",
   eprint = {1605.04923},
 primaryClass = "astro-ph.HE",
 keywords = {acceleration of particles, ISM: supernova remnants, Local Group, radio continuum: ISM},
     year = 2017,
    month = jan,
   volume = 464,
    pages = {2326-2340},
      doi = {10.1093/mnras/stw2566},
   adsurl = {http://adsabs.harvard.edu/abs/2017MNRAS.464.2326S},
  adsnote = {Provided by the SAO/NASA Astrophysics Data System}
}
```



The code is written with Python 2.7, although it should work with Python 3+. It should only require `numpy` and `matplotlib` installed.

### Installation
You can do the following :-
1. If you have [git](https://git-scm.com/) installed, you can directly clone this repository using `git clone https://github.com/sks67/s17lc.git` into your computer
2. Copy paste the `s17lc.py` into a blank `.py` file directly in your computer and use it accordingly.

### Description
The program `s17lc.py` is the coded up version of the equations A1-A11 in the paper. There are two main modules :-

1. `radius_velocity()`: This provides the radius and velocity of the supernova remnant for a given age, based on the dimensional variables and self similar solutions in [Truelove & Mckee 1999](http://adsabs.harvard.edu/abs/1999ApJS..120..299T). 

2. `luminosity()`: This provides the luminosity of the supernova remnant, given the radius, velocity, density and other parameters. 

### Usage
You can use these to create light curves or estimate values at a particular age. 

Either s17lc.py or rsnr.py can be used to do this.  

rnsr.py is ksl's adaptation of the original routine.  It contains a routine do_one that takes the parameters needed to define a SNR and generates a radio lightcurve as a function of diameter and time.  The results are contained in an astropy Table.  

### Updates by ksl
This version of the repository contains a new routine rsnr.py which isk ksl's rewwrite of the routines contained in s17lc.py and a new routine do_one which will generate a table of the radio luminosity as a function of time, given the parameters
one needs to describe the model.  The Jupyter notebooks BasicTest and Python3test were written as diagnostic routines for
this effort.  The Jupyter notebook test_s17lc needs files that were not procided in Sarbadhicary's git respostitory which 
can be found [here](https://github.com/sks67/s17lc)
