---
layout: lesson
title:  "Notebooks, part 2"
description: "Use Jupyter (an interactive notebook/analysis tool) for advanced visualization and analysis."
class_date:   2017-05-24
author: David Eads
copyright: 'This lesson is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">Creative Commons Attribution-ShareAlike 4.0 International License</a>.'
---

## Overview

Second part of notebooks lesson.

## Assignment

Due June 5, 2017.

### If you didn't make it to the first two classes

Work through [First Python Notebook](http://first-python-notebook.readthedocs.io/en/latest/) in this order:

Prologue, chapters 1-4, chapter 13, chapters 5-11, chapter 15.

### If you made it to the first class

Work through [First Python Notebook](http://first-python-notebook.readthedocs.io/en/latest/) in this order:

Chapters 7-11, chapter 15.

### Restart Jupyter

*On Windows:*

* Open cygwin
* Type `cd first-notebook`
* Type `jupyter notebook`

*On Mac:*

* Open terminal
* Type `cd first-notebook/first-python-notebook`
* Type `source bin/activate`
* Type `jupyter notebook`

### If you didn't make it to the third class

Once Jupyter is running, create a new text file and name it `utils.py`. Copy and paste the contents of [this link](https://gist.githubusercontent.com/eads/cab99b13aad9bd18255c927a809c0d00/raw/044818511774e12bfb3a48125a3b0b60e7001035/utils.py) into the file.

#### New notebook

Once Jupyter is running again, create a *new* Jupyter notebook.

Make sure the top of the file starts with a code cell that imports Pandas, Matplotlib, and our utilities:

```
%matplotlib inline
import pandas as pd
import utils
```

Create a Markdown cell describing your dataset and what you hope to accomplish with it.

Load a Socrata dataset without query parameters. For larger datasets, this could be slow, but will be cached for a day until it needs to download again. To do this, use the utility function I wrote for this purpose:

```
raw_data = utils.get_socrata_data("<URL-OF-DATASET>")
my_data = pd.DataFrame(raw_data)
```

Change `df` to a more descriptive variable name and replace `<URL-OF-DATASET>` with the full URL to your data, e.g. `http://data.cityofchicago.org/resource/cwig-ma7x.json`.

Now, inspect the data by creating code cells with `my_data.head()` and `my_data.info()`.

Finally, use the techniques described in class and the lesson to inspect columns, group, and sort.

At bare minimum, you should run some value counts on categorical / descriptive columns, e.g.

```my_data.COLUMN_NAME.value_counts().reset_index()```

For example, if you were looking at food inspections and had filtered the dataset, you could do something like ```failed_inspections.value_counts().reset_index()``` to see the business with the most failed inspections.

If you have a numeric column, you should try:

* Sum a numeric column (`my_data.NUMERIC_COLUMN_NAME.sum()`)
* Get basic descriptive statistics for the same column (`my_data.NUMERIC_COLUMN_NAME.describe()`)
* Make a basic chart (`my_data.NUMERIC_COLUMN_NAME.plot.bar()`)

If there are other techniques we covered in class that could apply to your analysis, try them out!

When you're done, go back to your terminal and stop Jupyter.

Check the status of your code with:

```
git status
```

Add your changes:

```
git add *.ipynb
```

Commit and describe your changes:

```
git commit -m "<DESCRIPTION OF WHAT YOU DID>"
```

Finally, push to Github:

```
git push
```

When you are satisfied, send me a link to your notebook on Github on Slack.

## Lesson

[First Python Notebook](http://first-python-notebook.readthedocs.io/en/latest/) by Ben Welsh, Chapters 7-11, 15.

