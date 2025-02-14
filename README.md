[Kaggle Scripts](https://www.kaggle.com/c/predict-west-nile-virus/scripts) are a great way to share models, visualizations, or analyses with other Kagglers.

You can run scripts right on Kaggle without ever downloading the data, but for iterating on your script, you'll probably find it's easier to work locally (and then copy your script to Kaggle for sharing).

## Directory Structure

It helps to set up the same directory structure that we have running on Kaggle. (Then you don't have to change any paths when copying the script to Kaggle.) [This file](https://www.kaggle.com/c/predict-west-nile-virus/download/west_nile.zip) sets up the directory structure (including all of the competition data):

- `input`: this contains all of the data files for the competition
- `working`: on Kaggle, scripts run with this as the working directory. We recommend you do the same thing locally to avoid mixing output files with source files.
- `src`: Source scripts. We've provided some examples to get you started.

## Python and R Environments

We have Github repositories showing our [R](https://github.com/Kaggle/docker-r) and [Python](https://github.com/Kaggle/docker-python) environments are set up. We plan to make it very easy to work with the exact same environment locally, but at this point it may be easier to work with whatever environment you already have. (If you use Python or R packages locally that turn out to be missing in our online environment, we can probably add them for you.)

Do make sure you're using Python 3, though. 

[Conda](http://conda.pydata.org/docs/intro.html) is great for managing Python environments.

## RMarkdown

If `src/measurement_locations.Rmd` is the RMarkdown file you want to render as HTML, you can say:

`Rscript render_rmarkdown.R src/measurement_locations.Rmd`

Then open `working/output.html` to view the results!

## Command Line Execution

In your shell, you can navigate to the `working` directory, and run a script by saying:

`Rscript ../src/measurement_locations.R`

or

`python ../src/measurement_locations.py`

# R

We all love RStudio for interactive work. If you open a script in `src` in RStudio, your working directory will probably default to `src`. So we've included a line in the example that switches you to `working` at the top of the script.


# Python

While we don't support iPython Notebooks in Scripts at this point, we know many people like to work in notebooks interactively. We've included an example notebook. The comments indicate the couple small changes required for transitioning to a script.





# West_nile_model
# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Kaggle Competition - Starter

## Introduction

Welcome to your first week of work at the Disease And Treatment Agency, division of Societal Cures In Epidemiology and New Creative Engineering (DATA-SCIENCE). Time to get to work!

Due to the recent epidemic of West Nile Virus in the Windy City, we've had the Department of Public Health set up a surveillance and control system. We're hoping it will let us learn something from the mosquito population as we collect data over time. Pesticides are a necessary evil in the fight for public health and safety, not to mention expensive! We need to derive an effective plan to deploy pesticides throughout the city, and that is **exactly** where you come in!

## Dataset

The dataset, along with description, can be found here: [https://www.kaggle.com/c/predict-west-nile-virus/](https://www.kaggle.com/c/predict-west-nile-virus/).

**This is also where you will be submitting your code for evaluation**. We will be using the Kaggle Leaderboard to keep track of your score. The public leaderboard uses roughly 30% of the dataset to score an AUC (Area Under Curve) metric. [You can read more about the scoring metric here](https://www.kaggle.com/wiki/AreaUnderCurve).

> If you do not already have a Kaggle account, you will need to sign up on the website.  Also note that you will be submitting a "Late Submission" on Kaggle because the official competition has ended.  You can use the leaderboard to see how your results compare against roughly 1300 other data science teams!

You can submit predictions as many times as you want to Kaggle, but there is a limit of 5 submissions per day.  Be intentional with your submissions!


#### Navigating Group Work

This project will be executed as a group.  To make your team as effective and efficient as possible you should do the create a shared GitHub repo and project planning document as described in the deliverables section below.

## Deliverables

**GitHub Repo**

1. Create a GitHub repository for the group. Each member should be added as a contributor.
2. Retrieve the dataset and upload it into a directory named `assets`.
3. Generate a .py or .ipynb file that imports the available data.

**Project Planning**

1. Define your deliverable - what is the end result?
2. Break that deliverable up into its components, and then go further down the rabbit hole until you have actionable items. Document these using a project managment tool to track things getting done.  The tool you use is up to you; it could be Trello, a spreadsheet, GitHub issues, etc.
3. Begin deciding priorities for each task. These are subject to change, but it's good to get an initial consensus. Order these priorities however you would like.
4. You planning documentation (or a link to it) should be included in your GitHub repo.

**EDA**

1. Describe the data. What does it represent? What types are present? What does each data points' distribution look like? Discuss these questions, and your own, with your partners. Document your conclusions.
2. What kind of cleaning is needed? Document any potential issues that will need to be resolved.

**Note:** As you know, EDA is the single most important part of data science. This is where you should be spending most of your time. Knowing your data, and understanding the status of its integrity, is what makes or breaks a project.

**Modeling**

1. The goal is of course to build a model and make predictions that the city of Chicago can use when it decides where to spray pesticides! Your team should have a clean Jupyter Notebook that shows your EDA process, your modeling and predictions.
2. Conduct a cost-benefit analysis. This should include annual cost projections for various levels of pesticide coverage (cost) and the effect of these various levels of pesticide coverage (benefit). *(Hint: How would we quantify the benefit of pesticide spraying? To get "maximum benefit," what does that look like and how much does that cost? What if we cover less and therefore get a lower level of benefit?)*
3. Your final submission CSV should be in your GitHub repo.

**Presentation**
* Audience: You are presenting to members of the CDC. Some members of the audience will be biostatisticians and epidemiologists who will understand your models and metrics and will want more information. Others will be decision-makers, focusing almost exclusively on your cost-benefit analysis. Your job is to convince both groups of the best course of action in the same meeting and be able to answer questions that either group may ask.
* The length of your presentation should be about 20 minutes (a rough guideline: 2 minute intro, 10 minutes on model, 5 minutes on cost-benefit analysis, 3 minute recommendations/conclusion).  Touch base with your local instructor... er, manager... for specific logistic requirements!

---

**Your project is due at 10:00 AM EST/9:00 AM CST on Friday, June 15.**

---

### Project Feedback + Evaluation

Data science is a field in which we apply data to solve real-world problems. Therefore, projects and presentations are means by which we can assess your ability to solve real-world problems in a data-driven manner.

Your final assessment ("grade," if you will) will be calculated based on a [topical rubric](https://docs.google.com/spreadsheets/d/1V6OzSHPXCJEe_sVT7B1vE7sT-jqNMNo-NrmZHtafMXY/edit?usp=sharing). For each category, you will receive a score of 0-3. From the rubric you can see descriptions of each score and what is needed to attain those scores. Make sure you look at the "Rubric P4" tab of the [spreadsheet](https://docs.google.com/spreadsheets/d/1V6OzSHPXCJEe_sVT7B1vE7sT-jqNMNo-NrmZHtafMXY/edit?usp=sharing).