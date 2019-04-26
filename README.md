# <img src="/tex/4c87ee198ded31321f89b44a38a0ad5a.svg?invert_in_darkmode&sanitize=true" align=middle width=21.552516149999988pt height=26.76175259999998pt/> confusion

The squared buoyancy frequency is defined as <img src="/tex/bd2177a908f1cd4fc2ab2dd25029bfff.svg?invert_in_darkmode&sanitize=true" align=middle width=96.71016959999999pt height=35.76220559999998pt/> where <img src="/tex/3f5d596c61b4bf3d7b4fe363ddd43d6d.svg?invert_in_darkmode&sanitize=true" align=middle width=32.28892919999999pt height=27.6567522pt/> is 
> "the difference between the potential densities of the two seawater parcels with the reference pressure being the average of the two original pressures of the seawater parcels." ([TEOS-10 Handbook, p. 32, eq. 3.10.2.](http://www.teos-10.org/pubs/TEOS-10_Manual.pdf)).

In the `gsw` package, this is implemented via the [`gsw_Nsquared(SA,CT,p,{lat})`](http://www.teos-10.org/pubs/gsw/html/gsw_Nsquared.html) function. Here, the argument `p` represents the absolute pressure in dbar.

<img src="/tex/4c87ee198ded31321f89b44a38a0ad5a.svg?invert_in_darkmode&sanitize=true" align=middle width=21.552516149999988pt height=26.76175259999998pt/> can also be calculated by hand via<br> 
<img src="/tex/23b83c12a18bbd188b918ace0f62f775.svg?invert_in_darkmode&sanitize=true" align=middle width=190.47030254999999pt height=24.65753399999998pt/> and <br>
<img src="/tex/0730cb95f7253f610e13686db8847038.svg?invert_in_darkmode&sanitize=true" align=middle width=201.38358899999997pt height=27.6567522pt/><br>
where <img src="/tex/7ed3103a1e05c3ecd552a24db69222e2.svg?invert_in_darkmode&sanitize=true" align=middle width=40.43809109999999pt height=20.09134050000002pt/> is the average pressure between two depths and the different references pressures <img src="/tex/94500c9bc37dbd222043219a34cb0175.svg?invert_in_darkmode&sanitize=true" align=middle width=244.0912221pt height=24.65753399999998pt/> dbar.

You can find the code for obtaining <img src="/tex/4c87ee198ded31321f89b44a38a0ad5a.svg?invert_in_darkmode&sanitize=true" align=middle width=21.552516149999988pt height=26.76175259999998pt/> via both methods in [n2_confusion.Rmd](https://github.com/chrisdane/n2_confusion/blob/master/n2_confusion.Rmd). With
```
<img src="/tex/3e245e65bd04a8373098644a79ae4254.svg?invert_in_darkmode&sanitize=true" align=middle width=970.66440075pt height=124.74886710000001pt/>N^2<img src="/tex/05f26fc129d9118e998434f347cbad8e.svg?invert_in_darkmode&sanitize=true" align=middle width=785.1132580499999pt height=24.65753399999998pt/>mathtt{p\_ref}<img src="/tex/c69c3d333d775aae8e70e0abca422bb5.svg?invert_in_darkmode&sanitize=true" align=middle width=6.39271709999999pt height=24.65753399999998pt/>mathtt{p\_ref}<img src="/tex/ad9a960e78ba413dd0147aaba37a61e4.svg?invert_in_darkmode&sanitize=true" align=middle width=581.5541489999999pt height=47.671232400000015pt/>20.125^{\circ}<img src="/tex/79ade84ef224421644caba03f4edf56c.svg?invert_in_darkmode&sanitize=true" align=middle width=66.21596684999999pt height=22.831056599999986pt/>47.375^{\circ} North gridbox of Locarnini et al. 2018 and Zweng et al. 2018 ([link](https://www.nodc.noaa.gov/OC5/woa18/)).

<br>
<img align="left" width="2000" src="_bookdown_files/bookdown_files/figure-html/n2_plot-1.png">

