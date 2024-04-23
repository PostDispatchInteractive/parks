With fewer park employees than there are parks in St. Louis, corners get cut
========================

* [What is this?](#what-is-this)
* [Assumptions](#assumptions)
* [How to reproduce](#how-to-reproduce)
* [Data caveats](#data-caveats)

What is this?
-------------

This repo contains data and code used for the May 4 (online) and May 5, 2019 (print) St. Louis Post-Dispatch story ["With fewer park employees than there are parks in St. Louis, corners get cut"](https://www.stltoday.com/news/local/metro/with-fewer-park-employees-than-there-are-parks-in-st-louis-corners-get-cut/article_18f11107-fec2-5e03-b5f9-85568ce2c9ed.html). The story was reported by [Jesse Bogan](https://twitter.com/JesseBogan) with data analysis done by [Janelle O'Dea](https://twitter.com/jayohday).

The instructions below will enable you to reproduce the results of our data analysis on your own computer. You can also see a [static version of our code and results](https://html-preview.github.io/?url=https://github.com/PostDispatchInteractive/parks/blob/master/parks.html) if you would rather avoid installing libraries and using Python.

Assumptions
-----------

The following things are assumed to be true in this documentation.

* You are using Python 3.8 or higher.
* You have [virtualenv](https://pypi.python.org/pypi/virtualenv) and [virtualenvwrapper](https://pypi.python.org/pypi/virtualenvwrapper) installed and working.

How to reproduce
----------------

To reproduce this data analysis, you'll need a working knowledge of virtual environments and Python.

First, enter the following commands on the command line to create a virtual environment and install the required libraries:
```
mkvirtualenv parks --python=python3
pip install -r requirements.txt
```

Next, extract the CSV files from the `Archive.zip` file. (Note: If the files don't automatically extract into a subfolder called `Archive`, then you should create that subfolder and move the CSVs into it.)

Finally, it's time to open the [Jupyter Notebook](https://jupyter.org/) file `parks.ipynb`, which shows the filtering and sorting we did to calculate the data points reported in the story. You can open the notebook with the following command, which should open a new window in your browser:
```
jupyter notebook parks.ipynb
```


Data caveats
-------------

The `Archive.zip` file contains the data used for this analysis, as downloaded on April 30, 2019 from the [Service Requests Dataset Distribution](https://www.stlouis-mo.gov/data/datasets/distribution.cfm?id=2) page on the St. Louis Open Data portal.

The data reflect complaints submitted by St. Louis city residents by phone, web, email or Twitter. Each row reflects one complaint.

The data dictionary can be found at the same Open Data portal link above, under the heading "Field Definitions."

The complaint data reflects only what has been reported to the city. Other issues at parks may exist and nobody calls them in.

There is a unique identifier for each complaint, `REQUESTID`, but there is not a unique identifier for the person who reported the complaint. So, it's not possible to know if the same person made all of the complaints about a particular park or if various people did.
