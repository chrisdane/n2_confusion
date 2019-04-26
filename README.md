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
git clone https://github.com/chrisdane/n2_confusion.git
```
you can reproduce the `html` version of the script ([n2_confusion/_book/n2-confusion.html](https://github.com/chrisdane/n2_confusion/blob/master/_book/n2-confusion.html)).

# Results

The plot shows absolute values of <img src="/tex/4c87ee198ded31321f89b44a38a0ad5a.svg?invert_in_darkmode&sanitize=true" align=middle width=21.552516149999988pt height=26.76175259999998pt/> (left), differences between the default method (GSW) and using different reference pressures <img src="/tex/fc768881d80481de1205a5c1e2d84ad3.svg?invert_in_darkmode&sanitize=true" align=middle width=40.43809109999999pt height=20.09134050000002pt/> (<img src="/tex/fc768881d80481de1205a5c1e2d84ad3.svg?invert_in_darkmode&sanitize=true" align=middle width=40.43809109999999pt height=20.09134050000002pt/> minus GSW; middle) and these differences as % of the default GSW method.

The underlying data is the World Ocean Atlas 2018 climatology (1955-2017) at the <img src="/tex/000ab2c0010ce8b67672421f43f5c84b.svg?invert_in_darkmode&sanitize=true" align=middle width=52.39746599999998pt height=22.63850490000001pt/> West and <img src="/tex/5735ed1a6ae514390f2a10a0a003f5e2.svg?invert_in_darkmode&sanitize=true" align=middle width=52.39746599999998pt height=22.63850490000001pt/> North gridbox ([Locarnini et al. 2018 and Zweng et al. 2018](https://www.nodc.noaa.gov/OC5/woa18/)).

<img align="left" src="_bookdown_files/bookdown_files/figure-html/n2_plot-1.png">

