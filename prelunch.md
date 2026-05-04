---
title: "Jupyter Notebook"
teaching: 30 # teaching time in minutes
exercises: 15 # exercise time in minutes
---

## 1. What Is a Python Notebook?

A **Notebook** is an interactive computing environment that allows you to combine:

- Code (Python)
- Text explanations
- Mathematical equations
- Tables and visualizations
- Results and outputs

All in a single document!

Jupyter Notebooks are especially useful for:

- Data exploration, cleaning, & analysis  
- Teaching and learning Python  
- Prototyping models  
- Sharing reproducible research  

Instead of writing a script and running it all at once, you work in **small, executable blocks called cells**. An example of this would be using the **Notebook** feature in ArcGIS Pro Desktop. 

---

## 2. Why Data Scientists Use Python Notebooks ?

Python Notebooks support an **iterative workflow**:

1. Write a few lines of code  
2. Run them immediately  
3. Inspect the output  
4. Modify and rerun as needed
5. Move on to next step and repeat!  

### Key Advantages

- Immediate visualization of data  
- Easy experimentation  
- Built-in documentation using Markdown  
- Reproducible analysis  
- Simple sharing with collaborators  

---

## 3. Getting Started: Opening a Notebook

You can use Jupyter Notebooks in several ways, one such way is:

- [Google Collab](https://colab.research.google.com). You would need a google account for this. Then create a new notebook in Drive. 

### Quick Start in Google Colab (easiest for beginners)

1. Go to https://colab.research.google.com
2. Click **File → New notebook**
3. You're ready! No installation needed.

![Opening a New Notebook in Colab.](colabintro.png "Google Colab")

#### Why Run this online ?

- Ease of Usage and Free 
- Colab runs in the cloud → you only need a Google account and internet 
- **Most** Python packages/libraries are pre-installed! 

---

:::::::::::::::::::::::::::::::::::::::::: challenge

##### Get Started with the Notebook

Work through the interactive Python notebook linked below, which covers everything on this page hands-on inside Google Colab.

**New to Python?** Start at cell 1 and work through cell 12 to build up the fundamentals — variables, lists, loops, and functions.

**Already comfortable with the basics?** Jump straight to cell 13 to explore NumPy, pandas, Matplotlib, and GeoPandas in action.

<a href="https://colab.research.google.com/github/SpatialTurn/IGIC2026/blob/main/episodes/intro_python.ipynb" target="_blank">Open the Notebook in Google Colab.</a>

::::::::::::::::::::::::::::::::::::::::::::::::::::::


**Note**: To SAVE your changes made, make sure to Save a copy of the notebook in your Drive! 

![](savecopy.png "Your Notebook")


## 4. What is a Python Library?

A Python library is a collection of pre-written code that you can bring into your own project to save time. Instead of writing everything from scratch, you import a library and immediately gain access to powerful tools that others have already built and tested.

You import a library using the `import` keyword:

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
```
The `as` keyword gives the library a shorter nickname — these aliases (`pd`, `np`, `plt`) are standard conventions you will see everywhere in data science code.

### Why Libraries Matter ?

Python on its own is a general-purpose language. Its real strength in data science comes from its ecosystem of libraries. A task that might take hundreds of lines of custom code — such as reading a CSV, computing statistics, and drawing a chart — can be done in fewer than ten lines when you use the right libraries.