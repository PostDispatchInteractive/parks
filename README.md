With fewer park employees than there are parks in St. Louis, corners get cut
========================

* [What is this?](#what-is-this)
* [Assumptions](#assumptions)
* [How to reproduce](#how-to-reproduce)
* [Data caveats](#data-caveats)

What is this?
-------------

This repo contains data and code used for the Aug. 7 (online and print) St. Louis Post-Dispatch story "Racial disparities in income and poverty remain stark, and in some cases, are getting worse". The story was reported by [Jacob Barker](https://twitter.com/jacobbarker) with data analysis done by [Janelle O'Dea](https://twitter.com/jayohday). 

Assumptions
-----------

The following things are assumed to be true in this documentation.

* You are running OSX.
* You are using Python 2.7. (Probably the version that came OSX.)
* You have [virtualenv](https://pypi.python.org/pypi/virtualenv) and [virtualenvwrapper](https://pypi.python.org/pypi/virtualenvwrapper) installed and working.

How to reproduce
-------------
To reproduce this data analysis, you'll need a working knowledge of virtual environments and Python. 

You'll need the libraries as specified in the `requirements.txt` file. To install the libraries, change into the `appraisals` directory, turn on your virtual environment and run the Terminal command `pip install -r requirements.txt`. 

Extract the data from the `.zip` file.

The code in the Jupyter Notebook file shows the filtering and sorting that was done to get the data points reported in the story. To see how we arrived at the data, run the code in the [Jupyter Notebook](https://jupyter.org/) file `appraisal_changes.ipynb`. 

Data
-----
The `Archive.zip` file contains the data used for this analysis. The 2019, 2015 and 2013 data are available on the city of [St. Louis Open Data portal](https://www.stlouis-mo.gov/data/). The Post-Dispatch obtained the 2017 data through a Sunshine request to the St. Louis Assessor. 
