## Formats for Ice2O Database
- **Dates**: YYYY-MM-DD
-  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; In Excel, this can be done by right-clicking -> Format Cells/ Number/ Custom, and typing 'yyyy-mm-dd' in the dialogue box.
- **Date and Time**: YYYY-MM-DD HH:MM:SS (on 24-hr clock)
- **Projection** - Alaska Albers (epsg 3338) prefered, but can transform on ingestion to database if not possible.
- **Format for Incoming Data** - csv prefered to tab-separated tables

# 'Tidy' Data

## Best practices for storing data
- Each variable forms a column
- Each observation forms a row
- Each observational unit forms a table

## Common Problems
- Column headers are values, not variable names. 
- Multiple variables are stored in one column. 
- Variables are stored in both rows and columns. 
- Multiple types of observational units are stored in the same table. 
- A single observational unit is stored in multiple tables.

For Example: observations stored as columns, not rows
![TidyData](/Ice2ODocs/images/NotTidy.png)

From Hadley Wickham's ['Tidy Data', 2014](https://www.jstatsoft.org/article/view/v059i10) Worth a read - much more relevant to day-to-day challenges than one might imagine!


# Project Organization, or, 'keepin' it all together'!
- Put each project in its own directory, which is named after the project.
- Put text documents associated with the project in the **doc** directory.
- Put raw data and metadata in the **data/raw/date** directory, and files generated during cleanup and analysis in a **data/processed/date** directory. This date mirrors **raw/date**, and reflects date collected, not processed. Source code for processing data should be placed in the **processed** folder as well; if processing was performed in Excel, or other non-coding environment, a README.txt should describe what processing was done to raw data, and how it was accomplished (repeatability!). A README.txt file should live in each data folder, and have the minimum information about source, and what has changed in each version of a dataset. 
- Put source for the project’s analysis in the **src** directory. Functions which are generalized and can be called in many anlysis scripts should be pulled out into a **functions** sub-folder. Scripts for data pre-processing/ cleaning that are used in multiple places (i.e. not appropriate to store in a single **processed** folder) go in a **munge** sub-folder.
- Name all files to reflect their content or function.

See an example folder structure below:

![folder2](/Ice2ODocs/images/FolderStructure.PNG)

From a combination of Software Carpentry's **"Good Enough Practices in Scientific Computing"** ([journal version](https://arxiv.org/abs/1609.00037), [dynamic version](https://swcarpentry.github.io/good-enough-practices-in-scientific-computing/)) and [A slightly different formulation](http://v4.software-carpentry.org/data/mgmt.html), also from Software Carpentry.

- Store data in a hierarchy of folders and files with regular names that can easily be pattern-matched.
- Use README files to store metadata.

# Data Management 
- Saving both raw and intermediate forms; documenting all steps; creating tidy data amenable to analysis.
- Software: writing, organizing, and sharing scripts and programs used in an analysis.
- Collaboration: making it easy for existing and new collaborators to understand and contribute to a project.
- Project Organization: organizing the digital artifacts of a project to ease discovery and understanding.
- Tracking Changes: recording how various components of your project change over time.
- Manuscripts: writing manuscripts in a way that leaves an audit trail and minimizes manual merging of conflict.

Also from Software Carpentry's ["Good Enough Practices in Scientific Computing"](https://arxiv.org/abs/1609.00037)
The detail on these broad points is very illuminating.

# Python Solutions
First thing's first: before installing any packages, [create a new environment](http://conda.pydata.org/docs/using/envs.html), so you don't inadvertently mess up the root environment. It's a good thing to always have a clean root you're always able to access, should something go wrong down the road.

If you're new(ish) to Python, downloading Anaconda is a great way to start. It comes bundled with many useful packages pre-compiled, and ready to use. 

To install a needed package try these (until one works):

```python
1. conda install package [on Anaconda]
2. pip install package
3. easy_install package
```

## Package Installation on Windows
As most users of Python are on linux/unix platforms, using windows can add a few wrinkles. At times, a python module you want will not be available for a windows machine on normal channels (conda, pip). Packages compiled for windows are available here: many thanks to the maintainers at UC Irvine!
[Wheel (.whl) package installation files for Python](http://www.lfd.uci.edu/~gohlke/pythonlibs/)

After downloading the package `cd` to the folder with download, and then `pip install filename` (be sure to use tab complete). Voila!

# SSL Issues inside the USGS Network
For further details on tackling SSL-related issues generated by working inside the USGS network, check out this 
[cheatsheet.](https://docs.google.com/a/doi.gov/document/d/18M6IHL_dfdypAHX8gUTr6LCsNRQA82rMdYfrEeBk6tg/edit?usp=sharing)

It's kept separately, as it relates to IT security, and is only accessible to USGS collaborators.

# Access to Network Drives
_Python_: `cd /D Q:` (for e.g. a drive named Q)

_Git_: (bash shell): `cd /q/`

# Fantastic Tutorials
 **Software Carpentry:**
 
 [Git and GitHub](http://swcarpentry.github.io/git-novice/)
 
 [Python Basics](http://swcarpentry.github.io/python-novice-inflammation/)
 
 [Databases and SQL](http://swcarpentry.github.io/sql-novice-survey/)
 
**Geohackweek (eScience):**

 [Rasters in Python](https://geohackweek.github.io/raster/)
 
 [Vector Data in Python](https://geohackweek.github.io/vector/)
 
 [Other Tutorials](https://geohackweek.github.io/)- links in calendar
 
 **Data Carpentry:**
 
 [Dos and Don'ts in Spreadsheet Design](http://www.datacarpentry.org/spreadsheet-ecology-lesson/)
 Data Carpentry has lots of great tutorials ... in R. At this point, the group is going with Python for open-source collaborations, but FYI :)
 
 # GitHub at the USGS
 
 # Header 1
 
 Sign up for aUSGS github account with your official email. [Directions here:](http://butst.usgs.gov/open-source/)
 
![Cat](/Ice2ODocs/images/cat.jpg)
 
 [Link to next page](Database Connection.md)
