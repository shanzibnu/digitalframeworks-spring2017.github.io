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

Due May 31, 2017.

### If you didn't make it to any classes

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

#### New notebook

Once Jupyter is running again, create a *new* Jupyter notebook.

Make sure the top of the file starts with a code cell that imports Pandas and Matplotlib:

```
%matplotlib inline
import pandas as pd
```

Create a Markdown cell describing your dataset and what you hope to accomplish with it.

Load a CSV dataset from a URL and assign it to a variable. Unless you find something else you'd like to investigate with a good dataset, one of the API urls you came up with from the web APIs assignment should be used. You can do this by creating a code cell like this:

```
my_data = pd.read_csv("<URL-OF-DATASET>")
```

Change `my_data` to a more descriptive variable name and replace `<URL-OF-DATASET>` with the full URL to your data.

Now, inspect the data by creating code cells with `my_data.head()` and `my_data.info()`.

Finally, use the techniques described in class and the lesson to inspect columns, group, and sort.

At the bare minimum, you should:

* Sum a numeric column (`my_data.NUMERIC_COLUMN_NAME.sum()`)
* Get basic descriptive statistics for the same column (`my_data.NUMERIC_COLUMN_NAME.describe()`)
* Make a basic chart (`my_data.NUMERIC_COLUMN_NAME.plot.bar()`)

If there are other techniques we covered in class that could apply to your analysis, try them out!

## Lesson

[First Python Notebook](http://first-python-notebook.readthedocs.io/en/latest/) by Ben Welsh, Chapters 7-11, 15.

