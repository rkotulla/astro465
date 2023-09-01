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
units of $erg s^{-1} cm^{-2} sr^{-2}$ via

$I = \frac{Flux}{solid angle} \rightarrow I = \frac{F}{\Omega} \times c_1$




## Empirical brightness profile models

## Color profiles

## Contour lines

# Project execution

## Prep work
1. Estimate the total field-of-view of the available CCD camera (see specs for
details). Based on this value, what would be a good value for log(D_25)?

## Target selection

From the [list of possible galaxies](galaxy_targets.html) select two galaxies of
different Hubble type (ideally one elliptical and one spiral galaxy) that a)
match the requirement for D_25 calculated above, and that are visible during
the observing semester.

Go to the [Hyperlede website](https://leda.univ-lyon1.fr/), then select the
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

Create a visibility chart for your two galaxies (XXX). Make sure to also
consider the lunar phase and the moon's proximity to your target (why does
this matter?)

## Execute Observations

## Data reduction

## Data analysis and interpretation

## Deliverables


[back](/)
