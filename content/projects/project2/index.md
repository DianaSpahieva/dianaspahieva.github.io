---
title: Project 2 - Jupyter & RMarkdown Tutorial
date: 2025-10-27 # to change
links:
  - type: site
    url: https://dianaspahieva.github.io/portfolio/blog/notebook-onboarding/ # to change
tags:
  - Jupyter
  - Markdown
---

Convert your Jupyter notebooks and RMarkdown documents directly into web posts with embedded code and outputs.

Hugo documentation - https://hugoblox.com/docs/guide/building/slides


Leverage your computational notebooks to publish reproducible research and tutorials:

- Export your Jupyter `.ipynb` or RMarkdown `.Rmd` files as markdown.
- Include executable code blocks, visualizations, and narrative text.
- Keep your website content in sync with your data and analysis pipeline.

This turns your scientific workflow into dynamic, online documents.

### Research Visualizations
![Analysis Plot 1](plot1.png)
{{< figure src="plot2.png" caption="Distribution of research results over time." numbered="true" >}}
You can add as many as you need by just referencing the filename!


### Analysis Walkthrough
{{< notebook
    src="demo_notebook.ipynb"
    show_code=false
    show_outputs=true
>}}

Customizing the View:
![Analysis Plot 4](plot4.png)