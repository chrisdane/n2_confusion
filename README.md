# n2_confusion

The buoyancy frequency is defined as <img src="/tex/bd2177a908f1cd4fc2ab2dd25029bfff.svg?invert_in_darkmode&sanitize=true" align=middle width=96.71016959999999pt height=35.76220559999998pt/> where <img src="/tex/3f5d596c61b4bf3d7b4fe363ddd43d6d.svg?invert_in_darkmode&sanitize=true" align=middle width=32.28892919999999pt height=27.6567522pt/> "the difference between the potential densities of the two seawater parcelswith the reference pressure being the average of the two original pressures of the seawaterparcels." ([TEOS-10 Handbook, p. 32, eq. 3.10.2.](http://www.teos-10.org/pubs/TEOS-10_Manual.pdf)).

In the `gsw` package, this is implemented via the [`gsw_Nsquared(SA,CT,p,{lat})`}(http://www.teos-10.org/pubs/gsw/html/gsw_Nsquared.html) function. Here, the argument `p` represents the absolute pressure in dbar.

Below, the differences between this default calculation of <img src="/tex/4c87ee198ded31321f89b44a38a0ad5a.svg?invert_in_darkmode&sanitize=true" align=middle width=21.552516149999988pt height=26.76175259999998pt/> as well as calculations by hand via
<p align="center"><img src="/tex/bbc28ba5b577fdb3533e0b6e836af36a.svg?invert_in_darkmode&sanitize=true" align=middle width=477.35936159999994pt height=18.3032784pt/></p>
where \verb|p_ref| = (0, 1000, 2000, 3000, 4000) dbar.

<br><br>
<img align="left" width="2000" src="_bookdown_files/bookdown_files/figure-html/n2_plot-1.png">

