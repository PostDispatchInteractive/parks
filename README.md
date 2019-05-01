parks
========================

* [What is this?](#what-is-this)
* [Assumptions](#assumptions)
* [How to reproduce](#how-to-reproduce)
* [Data caveats](#data-caveats)

What is this?
-------------

This repo contains data and code used for the "With fewer park employees than there are parks in St. Louis, corners get cut" Post-Dispatch story by Jesse Bogan

Assumptions
-----------

The following things are assumed to be true in this documentation.

* You are running OSX.
* You are using Python 2.7. (Probably the version that came OSX.)
* You have [virtualenv](https://pypi.python.org/pypi/virtualenv) and [virtualenvwrapper](https://pypi.python.org/pypi/virtualenvwrapper) installed and working.

How to reproduce
-------------

Data caveats
-------------
The `Archive.zip` file contains the data used for this analysis, as downloaded from https://www.stlouis-mo.gov/data/upload/data-files/csb.zip on April 30, 2019. 

The data reflect complaints submitted by residents of the city of St. Louis by phone, web, email or Twitter. Each row reflects one complaint. 

The complaint data reflects only what's reported to the city. Other issues at parks may exist and nobody calls them in. 

There is a unique identifier for each complaint, `REQUESTID`. There is not a unique identifier for who reported the complaint. Therefore, it's not possible to know if the same person made all of the complaints about a particular park or a number of different people did. 
