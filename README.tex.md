# $N^2$ confusion

The squared buoyancy frequency is defined as $N^2 \sim -\frac{g}{\rho} \frac{\Delta \rho^\Theta}{\Delta z}$ where $\Delta \rho^\Theta$ is 
> "the difference between the potential densities of the two seawater parcels with the reference pressure being the average of the two original pressures of the seawater parcels." ([TEOS-10 Handbook, p. 32, eq. 3.10.2.](http://www.teos-10.org/pubs/TEOS-10_Manual.pdf)).

In the `gsw` package, this is implemented via the [`gsw_Nsquared(SA,CT,p,{lat})`](http://www.teos-10.org/pubs/gsw/html/gsw_Nsquared.html) function. Here, the argument `p` represents the absolute pressure in dbar.

Below, the differences between this default calculation of $N^2$ as well as calculations by hand via
#$$
\begin{align*}
\rho = \mathtt{gsw\_rho(SA, CT, p\_mid)} \\
\rho^\Theta = \mathtt{gsw\_rho(SA, CT, p\_ref)} \,,
#$$
\end{align*}
where $\mathtt{p\_mid}$ is the average pressure between two depths and $\mathtt{p\_ref} = (0, 1000, 2000, 3000, 4000)$ dbar.

<br>
<img align="left" width="2000" src="_bookdown_files/bookdown_files/figure-html/n2_plot-1.png">

