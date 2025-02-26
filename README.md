[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/6jJdjMJC)
# Tabular Data Project: Survey Data Walkthrough 

## Assignment Summary 

For this project, students will use Python code (specifically Pandas) to work with one or more real-world, tabular datasets and communicate the insights they have gained from working closely with their selected data. Specifically, teams of 3-4 students will work with one or more prominent surveys that were conducted on national samples over periods of many years. Each team will create a curated subset around a focal area and will create a data guide (`.ipynb`, `.html`) for the subset. Students will be evaluated based on the quality of their technical implementations; their research and writing; and their success building on and effectively synthesizing multiple aspects of the tabular data unit.

## Assignment Purpose

This assignment asks students to fulfill the following learning goals:

1. Demonstrate the ability to load and work with one or more real-world, tabular datasets
2. Use tidy data structures and the split-apply-combine strategies in Python (using Pandas) to perform effective manipulations of your data, and support such code, where appropriate, with idiomatic Python
3. Move beyond a "recipe following" mentality that comes with first learning a method in order to synthesize what we have learned so far
4. Effectively communicate what we have learned using code, visuals, and text, culiminating with a polished `.html` report document
5. Use collaboration and version control to generate and document reproducible code

These learning goals are crucial to data analytics and computer science curriculum because tabular data is __the most common data format__ you are likely to encounter in either field. 

When working with other formats such as relational, hierarchical, and graph data, it is __typical to convert__ such data into a tabular format in order to perform common tasks like creating results pages, visualizing data, and conducting statistical analysis or machine learning. 

As we have seen, real-world data is often poorly structured, disorderly, incomplete, or otherwise difficult to work with. Completing this assignment is a chance to hone your data wrangling competency and demonstrate what you have learned so far in this class.  

## Assignment Files

To get started on this assignment, your team will visit the Github Classroom link and follow the assignment checkout process for team-based assignments. The Github Classroom link will be shared on Canvas. The assignment files will include data (or instructions on how to access data), metadata files, and a Jupyter Notebook assignment template  (`submission.ipynb`).

For projects, data (or data access instructions) will typically be located in the `data` folder of the Github Classroom repo. If there are supplemental resources for the datasets, such files will be located in the `meta` folder of the repo. Lastly, the Jupyter Notebook template (`submission.ipynb`) will typically have a mix of markdown and code blocks for you to get started. It is assumed that your team will modify this template as you go, including customized text for your title, subheadings, etc.

For this assignment, there are three datasets for your team to choose from. These datasets should look familiar, as you encountered them when completing your tabular data worksheets. For this assignment, we will dig deeper into how the the surveys were conducted, and what they can tell us about American life. 

__The General Social Survey (GSS)__ is a survey of adults in the United States that has been conducted anually since 1972. (Our dataset has responses from 1972 to 2022.) The GSS contains "a standard core of demographic, behavioral, and attitudinal questions" from year to year, and different questions pertaining to "topics of special interest" are included each year ("About").

The survey is cross-sectional rather than longitudinal, which means that the respondents for each year are always different. In a longitudinal study, in contrast, one group of respondents is selected and tracked for multiple years. The data can still help us understand social trends in the United States over time, but the survey's cross-sectional nature is an important limitation. 

__Note:__ The CSV files for this assignment are too large for the Github repository (>50 MB). You can access them via Google Drive by clicking this link: https://drive.google.com/drive/folders/11RalfoACwBjcjD8ETHKZqcAbayZC0MvR?usp=sharing

## Assignment Details

The core task of this assignment is to choose a focal area, create a curated subset of data on this topic, and create a data guide for the subset. This guide must include a specific set of technical components, but how and where you implement them is up to you.

__Topic or Focal Area:__

We have already seen several example topics in our worksheet assignments. Focal areas such as civic engagement, participation in religious life, and trust in institutions are all discussed in Robert D. Putnam's book _Bowling Alone_. Putnam draws on data from the GSS and triangulates his findings with the DDB Needham Life Style Surveys (DDB) and the Roper Social and Political Trends Data (RSP), along with other sources. The GSS includes various demographic variables that could be used for cross-tabulation. For example, have differences in male and female religiosity changed over time? 

To determine your topic, you can draw from Putnam and other scholars, read more about each survey online, and/or use your data munging skills in Python to find variables with multiple years of coverage, as we did in classwork and homework assignments.

__Your Data Subset:__

Your data subset should be based on your team's chosen topic, as well as the source data's coverage of that topic. 

Your subset should include a set of specific, inter-releated variables, as well as a clear date range. Your subset should be saved as a `.csv` file and included in your Github repository, and everything you include should be structed according to tidy data principles.

__Data Guide Submission:__ 

The data guide submission will mix Python code and markdown text to "walk through" your team's data subset, drawing on supplementary materials and outside resources. You will create it as a Jupyter Notebook file and submit it in both `.ipynb` and `.html` formats. Submissions should adhere to the following formatting guidelines: 

| Component               | Description                                                                                                                                                                                                 |
|:------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Title                   | Brief and informative, gives some idea of your topic area.                                                                                                                                                  |
| Introduction            | Include core background information and ethical considerations relevant to initial data collection and contemporary use of the data.                                                                        |
| Data Subset Description | Discuss the rationale for your subset and any strategies you used to decide on the topic area. Include a table of each selected variable, its data type, and examples of possible values for that variable. |
| Data Exploration        | Use a blend of descriptive statistics and data visualizations to explore the subset. Include code blocks. Discuss potential areas for deeper analysis based on the data.                                    |
| Uses of Python          | Take a step back and analyze your own use of code. Provide some rationale for choices you’ve made. Considerations may include performance, human readability, code dependencies, and reproducibility.       |
| References              | List all works cited in the data guide. Use proper APA format.

__Technical Components:__

Somewhere in your submission, your team is required to:

- use pandas to read data as DataFrame
- use at least one helper function of your own design, defined in Jupyter Notebook or imported from a local Python script (.py file)
- use pandas `groupby` with an aggregation method (`agg`, `count`, `first`, `max`, `sum`, `mean`, etc.)
- use pandas' `apply` method at least once to transform or create a variable  
- use pandas' `.loc`, `iloc`, or `.at` to filter data
- use three of the following utility methods from pandas: `sort_values`, `reset_index`, `set_index`, `fillna`, `dropna`, `astype`,  `rename`, `drop`, `head`, `tail`, `describe`
- use pandas to write data subset as `.csv` file or files
- use pandas' `cut` or `qcut` to create data bins 
- display inline at least one scatter plot, one line plot, one sequence of boxplots (using matplotlib, seaborn, etc.)

## Assessment Criteria 

Submissions will be evaluated on technical content; research and writing; and how well the submission comes together as a whole. The following descriptive rubric will be used when grading.

### Technical Content
- data files imported properly 
- attention is paid to the complexities of the source data (missing data, coded values, sample weighting, etc.)
- tabular data structures are used correctly, and tidy data standards are followed
- pandas operations and helper functions are used properly; submission uses all required code components correctly
- data visualizations are properly coded, sufficiently polished, and used effectively

### Research and Writing
- sufficient attention has been paid to proofreading
- external sources are used to enhance the submission, and sources are properly cited (APA style)
- the project is well organized, flows logically, and follows the all formatting guidelines
- the submission's use of language is appropriate for a well-informed, less technical reader

### Big Picture 
- all materials are turned in on time and in the right place
- assignment directions are followed, and all required components are included in the submission
- proper documentation and version control methods are used to facilitate collaboration and reproducibility
- the submission provides sufficient details or points to supplementary materials that make the research reproducible (e.g. detailed footnotes, appendices, links to GitHub, etc.)
- submitted materials build on multiple takeaways from the tabular data unit and synthesize them effectively

## Assignment Details

__Accessing assignment files:__ Via Github Classroom (linked on Canvas site)

__Teams:__ Assigned by instructor

__Required files:__ Jupyter Notebook (`.ipynb`) data guide, `.html` version (using "Download as" feature), any imported `.py` files, and `.csv` subset file or files.

__How to turn it in__: Upload `.html` on Canvas; upload or push `.ipynb` file, `.csv` files, all other project materials on Github

__Deadline:__ By the start of class on Monday, October 21, 2024.

## References 

About the GSS. (Retrieved January 4, 2024). https://gss.norc.org/About-The-GSS

Putnam, Robert. D. (2000). _Bowling Alone: The Collapse and Revival of American Community_. Simon and Schuster.

Roper Social and Political Trends. (Retrieved January 4, 2024). https://ropercenter.cornell.edu/featured-collections/roper-social-and-political-trends

```python

```
