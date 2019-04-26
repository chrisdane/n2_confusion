# n2_confusion

The buoyancy frequency is defined as $N^2 \sim -\frac{g}{\rho} \frac{\Delta \rho^\Theta}{\Delta z}$ where $\Delta \rho^\Theta$ 
> "is the difference between the potential densities of the two seawater parcelswith the reference pressure being the average of the two original pressures of the seawaterparcels." ([TEOS-10 Handbook, p. 32, eq. 3.10.2.](http://www.teos-10.org/pubs/TEOS-10_Manual.pdf)).

In the `gsw` package, this is implemented via the [`gsw_Nsquared(SA,CT,p,{lat})`}(http://www.teos-10.org/pubs/gsw/html/gsw_Nsquared.html) function. Here, the argument `p` represents the absolute pressure in dbar.

Below, the differences between this default calculation of $N^2$ as well as calculations by hand via
$$
\rho = \verb|gsw_rho(SA, CT, p_mid)| \\
\rho^\Theta = \verb|gsw_rho(SA, CT, p_ref)| \,,
$$
where $\verb|p_mid|$ is the average pressure between two depths and $\verb|p_ref| = (0, 1000, 2000, 3000, 4000)$ dbar.

<br><br>
<img align="left" width="2000" src="_bookdown_files/bookdown_files/figure-html/n2_plot-1.png">

