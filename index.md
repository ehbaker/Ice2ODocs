# 'Tidy' Data

### Best practices for storing data
- Each variable forms a column
- Each observation forms a row
- Each observational unit forms a table

From Hadley Wickham's ['Tidy Data', 2014](https://www.jstatsoft.org/article/view/v059i10)

# Scientific Computing

### Important steps to reproducibility, and group computing

Data Management: saving both raw and intermediate forms; documenting all steps; creating tidy data amenable to analysis.
- Software: writing, organizing, and sharing scripts and programs used in an analysis.
- Collaboration: making it easy for existing and new collaborators to understand and contribute to a project.
- Project Organization: organizing the digital artifacts of a project to ease discovery and understanding.
- Tracking Changes: recording how various components of your project change over time.
- Manuscripts: writing manuscripts in a way that leaves an audit trail and minimizes manual merging of conflict.

From Software Carpentry's ["Good Enough Practices in Scientific Computing"](https://arxiv.org/abs/1609.00037)

# Python Solutions
## Package Installation on Windows

First thing's first: before installing any packages, [create a new environment](http://conda.pydata.org/docs/using/envs.html), so you don't inadvertently mess up the root environment. It's a good thing to always a clean root you're always able to access, should something go wrong down the road.

To install a needed package try:
```markdown
```markdown
1. conda install package
2. pip install package
  - if an SSL error is thrown from within the network, add pypi as a trusted site for a single install with:
    pip install --index-url=http://pypi.python.org/simple/ --trusted-host pypi.python.org  package
3. 

 

*pygeoprocessing* on windows:
pip install --index-url=http://pypi.python.org/simple/ --trusted-host pypi.python.org  pygeoprocessing

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](img src="/images/cat.jpg")
<img align="left" src="/images/cat.jpg" width="250" height="250" />
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/ehbaker/Icefields-to-Oceans-Project-Data-Management/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
