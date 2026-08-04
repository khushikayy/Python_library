# 📊 Matplotlib Library Guide

![Python](https://img.shields.io/badge/Python-3.9%2B-blue)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Latest-brightgreen)
![License](https://img.shields.io/badge/License-MIT-yellow)

---

# 📖 Overview

**Matplotlib** is one of the most popular Python libraries for data visualization. It provides a comprehensive set of tools for creating static, animated, and interactive visualizations. Built on top of NumPy, Matplotlib allows users to generate high-quality graphs, charts, and plots for data analysis, scientific research, business reporting, and machine learning.

Matplotlib serves as the foundation for several other visualization libraries such as **Seaborn**, **Pandas Plotting**, and many scientific plotting tools.

It is widely used in:

- Data Science
- Machine Learning
- Scientific Computing
- Financial Analysis
- Business Intelligence
- Research
- Engineering
- Education
- Statistical Analysis

---

# ✨ Features

- Simple and intuitive plotting interface
- High-quality publication-ready figures
- Line, Bar, Scatter, Histogram, Pie, and Box plots
- 3D plotting support
- Customizable colors, fonts, and styles
- Interactive visualizations
- Animation support
- Multiple subplot layouts
- Integration with NumPy and Pandas
- Save figures in multiple formats

---

# 📦 Installation

## Install using pip

```bash
pip install matplotlib
```

## Install using conda

```bash
conda install matplotlib
```

## Verify Installation

```python
import matplotlib.pyplot as plt

print("Matplotlib installed successfully!")
```

---

# 📚 Requirements

- Python 3.9 or higher
- NumPy

Recommended Libraries

```
numpy   
pandas  
seaborn  
jupyter  
```

Install recommended packages

```bash
pip install numpy pandas seaborn jupyter
```

---

# 🚀 Quick Start

Import Matplotlib

```python
import matplotlib.pyplot as plt
```

Create a Simple Line Plot

```python
x = [1,2,3,4,5]
y = [2,4,6,8,10]

plt.plot(x,y)

plt.show()
```

---

# 📈 Basic Plot

```python
import matplotlib.pyplot as plt

x = [1,2,3,4,5]
y = [5,7,9,11,13]

plt.plot(x,y)
plt.title("Line Plot")
plt.xlabel("X-axis")
plt.ylabel("Y-axis")
plt.show()
```

---

# 📊 Line Plot

```python
plt.plot( x, y, color="blue", linewidth=2, linestyle="--", marker="o" )

plt.show()
```

---

# 📊 Bar Chart

```python
categories = ["A","B","C","D"]

values = [20,35,30,40]

plt.bar( categories, values, color="green" )

plt.show()
```

Horizontal Bar Chart

```python
plt.barh(categories, values)
```

---

# 🔵 Scatter Plot

```python
x = [1,2,3,4,5]

y = [5,7,8,7,10]

plt.scatter( x, y, color="red", s=100 )

plt.show()
```

---

# 📉 Histogram

```python
import numpy as np

data = np.random.randn(1000)

plt.hist( data, bins=30, color="orange", edgecolor="black" )

plt.show()
```

---

# 🥧 Pie Chart

```python
labels = ["Python","Java","C++","JavaScript"]

sizes = [40,25,20,15]

plt.pie( sizes, labels=labels, autopct="%1.1f%%" )

plt.show()
```

---

# 📦 Box Plot

```python
import numpy as np

data = np.random.randn(200)

plt.boxplot(data)

plt.show()
```

---

# 📈 Area Plot

```python
plt.fill_between( x, y, color="skyblue" )

plt.show()
```

---

# 📊 Multiple Plots

```python
plt.subplot(1,2,1)

plt.plot(x,y)

plt.subplot(1,2,2)

plt.bar(x,y)

plt.show()
```

---

# 🖼 Figure Size

```python
plt.figure(figsize=(10,6))
```

---

# 🎨 Colors and Styles

```python
plt.plot( x, y, color="purple", linestyle=":", marker="s", linewidth=3)
```

Available colors

```
red   
blue  
green  
yellow  
black  
purple  
orange  
pink  
cyan  
gray  
```

---

# 📝 Titles and Labels

```python
plt.title("Sales Report")

plt.xlabel("Month")

plt.ylabel("Revenue")
```

---

# 📌 Legends

```python
plt.plot( x, y, label="Sales" )

plt.legend()
```

---

# 📐 Grid

```python
plt.grid(True)
```

---

# 💾 Save Figures

PNG

```python
plt.savefig("plot.png")
```

PDF

```python
plt.savefig("plot.pdf")
```

SVG

```python
plt.savefig("plot.svg")
```

---

# 📊 Working with NumPy

```python
import numpy as np

x = np.linspace(0,10,100)

y = np.sin(x)

plt.plot(x,y)

plt.show()
```

---

# 📈 Working with Pandas

```python
import pandas as pd

df = pd.read_csv("sales.csv")

plt.plot(
    df["Month"],
    df["Sales"]
)

plt.show()
```

---

# 🌈 Plot Styles

List Available Styles

```python
print(plt.style.available)
```

Use a Style

```python
plt.style.use("ggplot")
```

Popular Styles

```
ggplot
classic
Solarize_Light2
bmh
dark_background
fast
fivethirtyeight
seaborn-v0_8
```

---

# 🎥 Animation

```python
from matplotlib.animation import FuncAnimation
```

Matplotlib supports animated charts for real-time and dynamic data visualization.

---

# 📊 3D Plotting

```python
from mpl_toolkits.mplot3d import Axes3D

fig = plt.figure()

ax = fig.add_subplot(
    111,
    projection="3d"
)
```

---

# 📚 Common Functions

| Function | Description |
|----------|-------------|
| plot() | Line plot |
| scatter() | Scatter plot |
| bar() | Vertical bar chart |
| barh() | Horizontal bar chart |
| hist() | Histogram |
| pie() | Pie chart |
| boxplot() | Box plot |
| fill_between() | Area plot |
| subplot() | Multiple plots |
| figure() | Create figure |
| title() | Add title |
| xlabel() | X-axis label |
| ylabel() | Y-axis label |
| legend() | Display legend |
| grid() | Show grid |
| savefig() | Save figure |
| show() | Display plot |

---

# ⚡ Best Practices

- Label axes clearly.
- Add meaningful titles.
- Use legends when plotting multiple datasets.
- Choose colors with sufficient contrast.
- Avoid cluttering charts with excessive information.
- Use appropriate chart types for your data.
- Save figures in high resolution for publication.
- Utilize styles for consistent visual appearance.

---

# 🧪 Example Project

```python
import pandas as pd
import matplotlib.pyplot as plt

df = pd.read_csv("sales.csv")

plt.figure(figsize=(10,6))

plt.plot(
    df["Month"],
    df["Sales"],
    marker="o",
    color="blue",
    linewidth=2
)

plt.title("Monthly Sales")

plt.xlabel("Month")

plt.ylabel("Sales")

plt.grid(True)

plt.savefig("sales_report.png")

plt.show()
```

---

# 🔥 Real-World Applications

- Sales and business dashboards
- Scientific research
- Machine learning model evaluation
- Statistical analysis
- Weather forecasting
- Financial market analysis
- Engineering simulations
- Healthcare analytics
- Image processing visualization
- Educational content

---

# 📖 Official Documentation

- https://matplotlib.org/
- https://matplotlib.org/stable/

---

# 👨‍💻 Acknowledgements

- Matplotlib Development Team
- NumPy Community
- Python Software Foundation

---

## ⭐ Support

If you found this project helpful:

- ⭐ Star the repository
- 🍴 Fork the repository
- 🐞 Report bugs
- 💡 Suggest improvements
- 📢 Share it with others

Happy Visualizing! 📊🚀