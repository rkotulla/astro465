---
layout: default
---

# Surface photometry of galaxies

## Background

Galaxies are conglomerates of stars, gas, dust and dark matter. They cover a
wide range in properties regarding the age of their stellar populations,
chemical properties, and kinematics. For example, galaxies along the Hubble
sequence can contain a spheroidal component (bulge) and/or a more flattened
component (disk), sometimes including other features such as rings and
bars. The luminosity contribution of stars in the bulge and disk changes
systematically along the Hubble sequence, with elliptical galaxies (also
called early-type galaxies) being entirely made up of a bulge, while spiral
galaxies (a.k.a. late-type galaxies) showing increasingly prominent disks at
the expense of the contribution from bulges as sub-types progress from Sa
(some disk with a prominent bulge) to Sd (almost entirely disk with little to
no bulge).

![alt text](hubble_sequence.png "Logo Title Text "Hubble sequence ")
Schematic drawing of galaxies along the Hubble sequence

The quantitative study of these structural components of galaxies with
the help of photometric and spectroscopic methods is essential to unravel the 
process  of galaxy formation and evolution. As such they revealed a wealth of
intrinsic correlations, such as the discovery of the fundamental plane of
galaxies as well as the luminosity-metallicity relation.

Integrated surface brightness photometry is one important tool of studying the
structure of galaxies. The goal of this approach is to measure the change of a
galaxy's integrated luminosity (which depends on wavelength; more on that
later) as a function of distance from the center of the galaxy. From this
so-derived surface brightness profile we can then derive the size, shape, and
relative contribution of its morphological components (bulge, disk, etc).

In this lab experiment you will learn to obtain the data for two galaxies and
derive their surface brightness profiles in two different bands. Fitting
empirical models then allows you to derive scale length for each of the
components, while the radial variation of the galaxy's color can shed some
light on its formation history.

## Terminology of surface brightness photometry

The goal of surface brightness photometry is to describe the two-dimensional
distribution of a galaxy's light emission in a standardized and
distance-independent manner. We thus require two main parameters: The actual
surface brightness $\mu$, expressed in magnitudes per square arcsec, and the
distance from the center of the source, $R_\star$, measured in arcsec.

We can convert observed fluxes $F$ measured on the CCD at position x,y during
each second (given in counts per second) to intensity $I(x,y)$ measured in
units of $erg\ s^{-1} cm^{-2} sr^{-2}$ via

$I = \frac{Flux}{solid angle} \rightarrow I = \frac{F}{\Omega} \times c_1$

where $\Omega$ is the solid angle of a single pixel, and $c_1$ a calibration
constant.

From that we can derive the surface brightness $\mu(x,y)$ at position (x,y)
from

$\mu(x,y) = -2.5 \times \log_{10}(F \times 1") + c_2$

with $c_2$ another calibration constant.

The surface brightness $\mu(x,y)$ is a measure of the intensity $I$ and
therefore independent of distance (why?) and an intrinsic property of the
galaxy, just as its absolute magnitude or color. However, we are looking for a
more standardized way to describe the intensity distribution of a
galaxy. Instead of the two coordinates x,y we can simply use the photometric
radius $R_\star$. Points of constant surface brightness are also named
"isophotes". For a given isophote at intensity level $F$ we can measure the
enclosed area $A(F)$. The photometric radius $R_\star$ of this isophote then
describes the radius of a circle with an  area equal to that of $A(F)$:

$R_\star = \sqrt(\frac{A(F)}{\pi})

$R_\star$ is therefore a measurement parameter defined by $A = A(>F)$,
increasing monotoneously as $F$ decreases. $R_\star$ is only determined by the
*area* of an isophoto, and **NOT** by its shape.

To derive the full surface brightness profile of a galaxy $\mu(R_\star)$ we
have to derive the photometric radii $R_\star$ for a number of isophotes
covering a range in intensities $F$. This technique has the major advantage of
much improved signal-to-noise ratios compared to simple one-dimensional cuts
through the galaxy, and can even be reliably derived for irregular galaxies
where straight-line cuts through the galaxy would depend heavily on the chosen
angle.


## Empirical brightness profile models

While each galaxy has its unique surface brightness profile, most galaxies
along the Hubble sequence can be approximated with one of the following
profiles:

### Exponential profile

Surface brightness profiles of disk galaxies can be approximated with an
exponential profile (see de Vaucouleur 1959, Freeman 1970) of the form

$I(R_\star) = I_0 \exp(-\exp{R}{\alpha})$

with $I_O$ being the central Intensity (units: $erg\ s^{-1} cm^{-2} sr^{-1}$)
and $\alpha$ being the exponential scale length (units: arcsec). Converted to
surface brightness the profile would be

$\mu(R_{\star}) = \mu_0 + 1.086 \times \frac{R_\star}{\alpha}$

The central surface brightness $\mu_0$ and exponential scale length $\alpha$
can be determined from a linear regression fit to the observed surface
brightness profile. If one plots the surface brightness as a function of
photometric radius $R_\star$, the contributions from the disk can be
identified from the linear part of the profile.

In addition to disk galaxies, this exponential profile also provides a agood
approximation to SBPs of spheroidal components in low-mass galaxies, such as
dwarf-irregular (dIrr) and dwarf-elliptical (dE) galaxies.


### de Vaucouleur profile

The de Vaucouleur profile (de Vaucouleur 1948, 1953) gives a good
approximation to the SBPs or elliptical galaxies and the bulge-component of
spiral galaxies. It describes the intensity profile by

$I(R_\star) = I_0 \times \exp(-\kappa R_{\star}^{\frac{1}{4}})$

with $I_0$ being the central surface brightness density, or in its alternative
form

$I(R_\star) = I_e \exp\left( -7.67 \times \left[ \frac{R_\star}{R_e}^{1/4} -1 \right] \right)$

$I_e$ marks the intensity at the effective radius R_e ($I(R_\star=R_e)$), that
is at the radius that contains half the total luminosity.

SBPs that match the de Vaucouleur profile form a straight line when plotting
$mu(R)$ as a function of $R_\star^{1/4)$.

### Sersic profile

The sersic profile (Sersic 1968) is a generalized form of the exponential law,
of the form

$I(R_\star) = I_0 \exp\left( -\frac{R_\star}{\alpha} \right)^{(1/\eta)} $

or alternative, for surface brightness:

$\mu(R_\star) = \mu_0 + 1.086 \times \left( \frac{R_\star}{\alpha}
\right)^{(1/\eta})$

For the special case of $\eta=1$ the Sersic profile is identical to the
exponential profile. In the case of $\eta=4$ the Sersic profile turns into the
de Vaucouleur profile (for $\eta=0.5$ the profile describes a gaussian
profile). Typical values for the Sersic index $\eta$ range from $\approx 3$ to
$\approx 6$ for ellptical galaxies, with smaller values for disk galaxies.




## Color profiles

A radial color profile can be computed by subtracting two surface brightness
profiles of a galaxy in two different (broadband) bandpasses. For example, the
g-r color profile can be derived from the g-band and r-band profiles as

$g-r = \mu_g(R_\star) - \mu_r(R_\star) = -2.5
\log_{10}\left(\frac{F_g}{F_r}\right) + c`$

From these color profiles we can gain insights into stellar populations as
function of distance from the galaxy center. Radial profiles of elliptical
galaxies, for example, show very little variation with radius, suggesting that
all stars are roughly the same age no matter where in the galaxy we
look. Galaxies with ongoing star formation, and in particular in the case of
starbursts, can show significant color gradients, resulting from very
different stellar populations in different radial regions. 


## Contour lines

t.b.d.




# Project execution

## Prep work

Estimate the total field-of-view of the available CCD camera (see specs for
details). Based on this value, what would be a good value for log(D_25)?

## Target selection

From the [list of possible galaxies](galaxy_targets.html) select two galaxies of
different Hubble type (ideally one elliptical and one spiral galaxy) that a)
match the requirement for D_25 calculated above, and that are visible during
the observing semester.

Go to the [Hyperleda website](https://leda.univ-lyon1.fr/), then select the
[SQL search](https://leda.univ-lyon1.fr/fullsql.html). This allows you to
define what galaxies might be suitable. In the **"WHERE"** field, enter

```SQL
de2000 > 0 and bt < 11
```

and in the **order** field enter al2000 (this will sort the resulting catalog
by right ascension, making it easier to find what galaxies are up at this time
of year)

This will select all galaxies with declination > 0 (de2000 > 0) and a total
B-band magnitude brighter than 11th magnitude. 

![alt text](hyperleda_sql.png "Hyperleda SQL interface")

Create a visibility chart for your two galaxies (XXX). Make sure to also
consider the lunar phase and the moon's proximity to your target (why does
this matter?)

## Execute Observations

## Data reduction

Using your jupyter notebook created in one of the previous sessions, reduce
your observed data frames by applying bias, dark, and flat-field corrections.
Equally important are the photometric calibration of your final images. This
can be achieved by comparing the observed (instrumental) magnitude of several
stars in your data with the cataloged magnitudes obtained e.g. from SDSS or
the LegacySurvey.

**add more details here**


## Data analysis and interpretation

## Deliverables

* Surface brightness profiles in each band, for each galaxy

* Color-profile for each galaxy

* Show that, for exponential disk galaxies, for a given central surface
 $\mu_0$ and scale length $\alpha$ the total apparent magnitude can be
 described as $m=\mu_0 + 5\log_{10}(\alpha) -2$.

* What is the relationship between effective radius $r_e$ and the exponential
scale length $\alpha$ for disk galaxies; and what is the mean surface
 brightness within $R_e$?

* From the derived apparent magnitude of each galaxy, what is he _absolute
  magnitude_ of the bulge and disk components? How many solar luminosities
  does that absolute magnitude correspond to in g and r-band?

* What mean surface brightness corresponds to a surface density of $1
  L_{\odot}/pc^2$?

* What was the mean sky brightness during the observations?

* Using Figure XXX, estimate an approximate stellar population age for the
  galaxy as a whole, and separately for its bulge and disk components.

* For the spiral galaxy: Derive the bulge to disk ratio from the integrated
  luminosities of disk and galaxy as a whole:

  $\frac{B}{D} = \frac{\rm total\ luminosity\ of\ galaxy}{\rm luminosity\ of\ disk} - 1$

  How does this value compare to expectations based on the classification of
  the galaxy along the Hubble sequence? Note that you need **luminosities**
  here, **not** magnitudes

* Investigate the residual image (i.e. the image of your galaxy after
  subtracting the model image reconstructed from your SBP data). Does your
  galaxy show any interesting features or peculiarities?

* What was the seeing at the time of your observations? You can derive this as
  the full width at half maximum width of a star observed in one of your
  galaxy images.
  


[back](/)
