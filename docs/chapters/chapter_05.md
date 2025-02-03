# Creating Scientific Visualisations

Scientific visualisations are essential for making complex data and concepts more accessible and interpretable. This chapter provides a practical guide to creating high-quality visualisations using a range of tools, including traditional programming libraries, diagram creation software, and AI-powered solutions. Best practices for embedding visuals into documents and web pages will be provided.

## 5.1. Overview of Scientific Visualisations

A scientific visualisation is the process of representing scientific data graphically to enhance understanding, interpretation, and communication. It transforms complex datasets into visual formats, such as **graphs**, **charts**, **maps**, and **3D models**, making patterns, trends, and relationships more accessible.


### 5.1.1. Importance of visuals in making scientific concepts accessible.

**Enhancing Comprehension**: Visuals help convey complex scientific data in an intuitive and digestible manner, making information easier to understand.

**Facilitating Pattern Recognition**: Graphs and charts highlight trends and correlations that might not be immediately apparent in raw data.

**Improving Communication**: Well-designed visuals allow scientists to effectively share findings with both experts and non-experts.

**Supporting Decision-Making**: In fields like medicine and environmental science, data visualisations aid in making evidence-based decisions.

**Engagement and Retention**: Research shows that visual content is processed faster and remembered longer compared to text-based information.


### 5.1.2. How Scientific Visualisations Differ from General Data Visualisations

**Purpose and Context**: Scientific Visualisations are used in research and academia to represent complex datasets, simulations, or models in fields like bioinformatics, physics, and climate science. General Data Visualisations, were commonly used in business, marketing, and journalism for trend analysis, performance metrics, and storytelling.

**Complexity of Data**: Scientific visualisations often deal with multidimensional, high-resolution, or real-time data requiring advanced computational techniques. General data visualisations typically present summarised trends in simple formats like bar charts and pie charts.

**Precision and Accuracy**: Scientific visualisations must adhere to strict accuracy standards to ensure reproducibility and credibility. General visualisations may prioritise aesthetics and simplicity over absolute precision.


## 5.2. Tools for Creating Visualisations - Traditional tools

### 5.2.1. R (ggplot2)

**Installing ggplot2**

To install and load ggplot2 in R, use the following commands:

install.packages("ggplot2")
library(ggplot2)

**Creating a Basic Scatter Plot**

data(mtcars)
ggplot(mtcars, aes(x = wt, y = mpg)) +
  geom_point() +
  labs(title = "Scatter Plot of Car Weight vs. MPG", x = "Weight", y = "Miles Per Gallon")

**Customising Colours, Legends, and Axes**

ggplot(mtcars, aes(x = wt, y = mpg, colour = factor(cyl))) +
  geom_point(size = 3) +
  scale_colour_manual(values = c("red", "blue", "green")) +
  labs(title = "Scatter Plot of Car Weight vs. MPG", colour = "Cylinders")

### 5.2.2. Python (Matplotlib, Seaborn, Plotly)

**Creating a Simple Plot with Matplotlib**

import matplotlib.pyplot as plt

x = [1, 2, 3, 4, 5]
y = [10, 20, 25, 30, 40]

plt.plot(x, y, marker='o', linestyle='-', color='b')
plt.xlabel("X-axis")
plt.ylabel("Y-axis")
plt.title("Basic Line Chart")
plt.show()

**Using Seaborn for Advanced Statistical Visualisations**

import seaborn as sns
import pandas as pd

#Load example dataset
data = sns.load_dataset("iris")
sns.pairplot(data, hue="species")
plt.show()

**Generating Interactive Charts with Plotly**

import plotly.express as px

data = px.data.gapminder()
fig = px.scatter(data, x="gdpPercap", y="lifeExp", color="continent", size="pop", hover_name="country", log_x=True)
fig.show()

## 5.3. Tools for Creating Visualisations - Diagram tools

**BioRender**

BioRender is an intuitive online platform for creating scientific illustrations. To use it:

Sign up at BioRender.

Use pre-made icons and templates to create high-quality biological diagrams.

Export your final visual in PNG, SVG, or PDF format.

**Inkscape**

Editing Vector Graphics in Inkscape

Download and install Inkscape.

Open an existing SVG file or create a new document.

Use the Pen Tool, Shapes, and Layers to create and modify diagrams.

Export the file in PNG, PDF, or SVG format.

**Graphviz**

Generating Automated Graph Structures

Graphviz allows users to create structured graphs and flowcharts using DOT language.

digraph G {
    A -> B;
    B -> C;
    C -> A;
}

To render a Graphviz file, use:

dot -Tpng input.dot -o output.png


## 5.4. AI Tools for Visualisations

How AI is transforming scientific visualisation.
Benefits of AI tools: automation, speed, accessibility, and enhanced creativity.
AI's role in generating complex visualisations from natural language or structured data.
**Advantages**: Faster creation, automation, accessibility for non-experts.
**Limitations**: Potential loss of control over detail, need for manual refinements.

**Napkin AI**

Napkin AI is a tool that simplifies the creation of scientific diagrams through AI-powered automation.

Converts natural language descriptions into structured diagrams.
Supports concept maps, flow diagrams, and data-driven charts.
Generates visually appealing and scientifically accurate graphics.

Example Workflow:
Enter a description (e.g., "Generate a flowchart of the DNA replication process").
AI processes the input and suggests an optimised diagram.
Customise the visual and export in PNG, SVG, or PDF formats.

How Napkin AI simplifies diagram creation and ideation through natural language inputs.
Use cases: Generating concept maps, flow diagrams, and data-driven visuals quickly.
Creating diagrams from text inputs using Napkin AI
Enhancing flowcharts and concept maps with AI

**Other AI tools**

DeepDream Generator (Google): AI-powered visual enhancements and artistic rendering.
Tableau GPT: AI-enhanced data visualisation for interpreting large datasets.
DALL·E: AI-generated scientific illustrations from text descriptions.

## 5.5. Embedding Visuals

Best practices for saving and exporting visuals (SVG, PNG, or PDF formats).
Integrating visuals into Markdown and HTML.
