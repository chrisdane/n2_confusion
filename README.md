# n2_confusion

The buoyancy frequency is defined as <img src="/tex/bd2177a908f1cd4fc2ab2dd25029bfff.svg?invert_in_darkmode&sanitize=true" align=middle width=96.71016959999999pt height=35.76220559999998pt/> where <img src="/tex/3f5d596c61b4bf3d7b4fe363ddd43d6d.svg?invert_in_darkmode&sanitize=true" align=middle width=32.28892919999999pt height=27.6567522pt/> 
> "is the difference between the potential densities of the two seawater parcelswith the reference pressure being the average of the two original pressures of the seawaterparcels." ([TEOS-10 Handbook, p. 32, eq. 3.10.2.](http://www.teos-10.org/pubs/TEOS-10_Manual.pdf)).

In the `gsw` package, this is implemented via the [`gsw_Nsquared(SA,CT,p,{lat})`}(http://www.teos-10.org/pubs/gsw/html/gsw_Nsquared.html) function. Here, the argument `p` represents the absolute pressure in dbar.

Below, the differences between this default calculation of <img src="/tex/4c87ee198ded31321f89b44a38a0ad5a.svg?invert_in_darkmode&sanitize=true" align=middle width=21.552516149999988pt height=26.76175259999998pt/> as well as calculations by hand via
<p align="center"><img src="/tex/29151556b83ccbc3ed09ac9151b82ba4.svg?invert_in_darkmode&sanitize=true" align=middle width=458.77491495000004pt height=18.3032784pt/></p>
where <img src="/tex/7c3d586c7ca43c806a671e3804186047.svg?invert_in_darkmode&sanitize=true" align=middle width=43.15033964999999pt height=20.09134050000002pt/> is the average pressure between two depths and <img src="/tex/eddc34ae78172eb9bdd91215a3162804.svg?invert_in_darkmode&sanitize=true" align=middle width=246.80346569999998pt height=24.65753399999998pt/> dbar.

<br><br>
<img align="left" width="2000" src="_bookdown_files/bookdown_files/figure-html/n2_plot-1.png">

