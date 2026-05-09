---
title: "Setup"
---

## Workshop Overview

**Enabling the Geospatial Turn through Cyberinfrastructure Training**  
🌐 <https://spatialturn.github.io/IGIC2026/>

This workshop introduces Jupyter Notebook as a platform for data analysis using U.S. Census data as a practical case study. Participants will learn how to access, clean, analyze, and visualize data while understanding key Census concepts such as variables and geographic units.

Designed for beginners, the session emphasizes hands-on learning and guides participants through a complete workflow — from data acquisition to interpretation. **Basic Python experience is required.**

---

## Schedule

| Time | Session | Content | Activities |
|------|---------|---------|------------|
| 9:00 – 10:00 | Notebook Basics | Introduction to Jupyter Notebook and Google Colab | Open notebook, run first code cell, create markdown notes |
| 10:00 – 11:00 | Python Libraries | Importing libraries (GeoPandas, pandas, matplotlib, NumPy) | Use libraries, create variables, load sample data, short exercise on data exploration |
| 11:00 – 12:00 | Introduction to Census Data | American Community Survey (ACS) vs. Decennial Census | — |
| 12:00 – 1:00 | *Lunch Break* | — | — |
| 1:00 – 2:00 | Accessing Census Data | Download data or access via the Census API | Retrieve data, convert to DataFrame, explore dataset structure, variables, tables, columns, and geographic units |
| 2:00 – 3:00 | Data Cleaning & Analysis | Cleaning data, renaming fields, sorting, summary statistics | Clean dataset, identify top counties, basic analysis |
| 3:00 – 4:00 | Visualization | Creating charts and maps of population trends | Maps and charts of population distribution, interpreting results |

---

## Setup Requirements

To participate in this workshop, you will need:

We offer **two setup paths**:

1. **Google Colab** — recommended for beginners; no installation needed
2. **Local installation** with Anaconda Navigator — for offline work and full control

---

### Option 1: Google Colab (Zero Installation – Recommended)

Google Colab is a free, cloud-based Jupyter notebook environment hosted by Google. It runs entirely in your browser, requires only a Google account, and comes with pandas, matplotlib, seaborn, and many other data science libraries **pre-installed**.

#### Steps

1. Go to <https://colab.research.google.com>
2. Sign in with your Google account (or create one if needed).
3. Click **New notebook** (or **File → New notebook**).
4. *(Optional)* Rename it: **File → Rename** (e.g., `Data Viz Workshop – YourName`).
5. Test the libraries by running this in the first cell (`Shift+Enter` to execute):

```python
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
import plotly.express as px   # optional – usually pre-installed

print("pandas version:", pd.__version__)
print("matplotlib version:", plt.matplotlib.__version__)
print("seaborn version:", sns.__version__)
print("plotly version:", px.__version__ if 'px' in globals() else "not imported")

## Quick test plot (should appear inline)
tips = sns.load_dataset("tips")   # built-in Seaborn dataset
sns.histplot(data=tips, x="total_bill", hue="time")
plt.title("Test: Restaurant Tips Distribution")
plt.show()
```

6. If a package is missing or needs updating, install it with:

```python
!pip install --upgrade seaborn plotly
```

> The `!` prefix runs shell commands inside a Colab or Jupyter cell.

#### Advantages of Colab for this workshop

- No software installation required
- Free GPU/TPU access if needed later
- Easy sharing via **File → Share**
- Autosaves to Google Drive
- Perfect for following along with instructor demos

**Tip:** Upload your own data files using the left sidebar (**Files → Upload**), or mount Google Drive:

```python
from google.colab import drive
drive.mount('/content/drive')

# Then read files like:
# pd.read_csv('/content/drive/MyDrive/penguins.csv')
```

---

### Option 2: Local Installation (Anaconda Navigator)

Use this option if you prefer working offline or need a persistent local environment.

1. Download and install **Anaconda Navigator**:
   - <https://www.anaconda.com/products/navigator>
   - Choose your OS installer (Python 3.x version) and follow the default prompts.

2. After installation, launch **Jupyter Notebook** from the Anaconda Navigator home screen.

3. To install any missing packages, add the following to a code cell and run it:

```python
!pip install <package-name>
```

---

## Troubleshooting

| Problem | Fix |
|---------|-----|
| **Colab:** plots not showing | Add `%matplotlib inline` at the top of the notebook (usually automatic) |
| **Local:** `ModuleNotFoundError` | Run `!pip install <package-name>` in a code cell |
| **General help** | Raise your hand during the workshop, or check the [Carpentries Python setup guide](https://swcarpentry.github.io/python-novice-gapminder/setup.html) |

---

You're all set! Proceed to **Introduction to Data Visualization** or **Creating Your First Plots**.

*Happy visualizing!*