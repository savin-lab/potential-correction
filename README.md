Correction scheme for a potential measured by particle tracking
=======

A notebook implementing the algorithm to correct an energy landscape, as measured by particle tracking, for static and dynamic errors.

---
## Citation

**Errors in energy landscapes measured with particle tracking**  
Michał J. Bogdan and Thierry Savin, _Biophys. J._ **115**:139-149 (2018)  
http://doi.org/10.1016/j.bpj.2018.05.035

```
@article{Bogdan:2018,
  author = {Bogdan, Micha\l{} J. and Savin, Thierry},
  title = {Errors in energy landscapes measured with particle tracking},
  volume = {115},
  number = {1},
  pages = {139--149},
  year = {2018},
  doi = {10.1016/j.bpj.2018.05.035},
  URL = {http://doi.org/10.1016/j.bpj.2018.05.035},
  eprint = {http://www.cell.com/biophysj/fulltext/S0006-3495(18)30675-1},
  journal = {Biophysical Journal}
}
```

---
## Requirements

* Wolfram Mathematica is required to execute the notebook. It can be obtained from http://www.wolfram.com/mathematica.
* The input data files should be provided as three columns .csv files:
 +  1st column: locations at which the apparent potential is measured;
 +  2nd column: values of the measured potential;
 +  3rd column: error bars on the potential's measurements.

---
## Files

  + "`Potential-Correction.nb`" is a Mathematica notebook implementing the true potential reconstruction algorithm using Eqs. (15) & (16) of the article referenced above;
  + "`Examples/`" contains 8 example data files, with the simulation results used to generate Fig. 5 of the article; the names of the files provide information about which of the curves the data refers to: for example, "`Data_fig5a_sig0.1_eps0.3_p10.csv`" contains the data for Fig. 5a, with the dimensionless shutter time `sigma=0.3`, the dimensionless static localisation uncertainty `epsilon=0.3`, and the optimal polynomial order of potential fitting `p=10`.

---
## Structure of the notebook

* The section **INPUTS** specifies the information to be entered by the user;
* The section **CALCULATIONS** performs the reconstruction algorithm;
* The section **OUTPUTS** plots the reconstructed potential compared to the apparent measured potential, and gives the polynomial coefficients of the reconstructed potential.
