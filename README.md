[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/stuartmac/sweet-jupy/master)

# sweet-jupy
Exploring Jupyter notebooks for research software development.

These notebooks illustrate the points I want to discuss at the CB RSE Skill Share 
(31st May 2019, Dundee University).

The topics I will try to cover are:

## Notebook Structure 

What should we consider when organising a notebook? What options do we have?

### Cell interdependence
Gotcha: cell run order and object states

### Setup cells

### Self-contained cells?
*I think a good caching strategy solves all these problems*

This isn't something I  advocate but you could try to have each cell executable on
its own after a kernel restart. To do this you would need to repeat all the relevant
imports in every cell and reload/ reconstruct any data you need.

For the notebook as a whole I think all the redundant duplication would have a negative
impact on readibility but it *might* actually be neat to be able to see everything that
goes into a single cell output.

To do this "efficiently" I think you would need to write all transformed data to disk
so you could reload it in the next cell. Otherwise, each cell relying on a modified
object would need to contain all its antecendent's code to remain independent.

Repeated module imports shouldn't cost anything as far as runtime goes but constantly
loading and persistening data would definetely affect cell performance. There is a flipside
though in that you wouldn't need to rerun the whole notebook after a restart.

## Better Project Organisation with Multiple Notebooks
### Advantages to avoiding monoliths
### Data exchange
### How far to go: abstration paradigms

## Cluster submission

## Favourite plugins
