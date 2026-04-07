
# 📆 Final project milestone (Due on 4/17)

### The goal of the Milestones is to follow your progress on your final project and identify challenges that your group might be facing. By April 17, I would like to see:

1. An expanded version of the README file describing in detail:
- Problem statement, question(s) and/or objective(s)
- Datasets you will use (with links, if available)
- Tools/packages you’ll use (with links)
- Planned methodology/approach
- Present or anticipated challenges

2. A project board with large tasks broken down into standalone issues assigned to the respective group member(s) responsible for tackling it.

3. Evidence (in the form of commits, issues, comments) that all group members are participating

4. One or more development notebooks that contain one or more data exploration plots (remember to check out the [Chart Suggestion – A Thought-Starter ](https://github.com/orgs/GPGN268/discussions/6) from our GitHub discussion)


### Notes about collaborating on GitHub

Collaboration can be a bit more complicated with Jupyter notebooks (vs. standalone Python scripts/libraries) since running cells in the notebook will change execution count and output, even if the code and content appear identical. **Best practice is to avoid situations where two people are independently working on the same notebook**. 

**General recommendation** - Split the project into multiple smaller notebooks and have each person work on different components. Avoid the long mega-notebook (like most of our labs) and instead structure your repo with a series of notebooks. For example, you could have one notebook that ingests files, reduces/manipulates the data (e.g., reprojection), then writes new files out to disk in “analysis-ready” format. Then a second notebook reads in those data and does some analysis, creates some plots, etc. If you can pass things back and forth between group members like this, you’ll avoid conflicts (conflicts are the worst!).

**Alternative recommendation** – Each team member can create separate notebooks with different filenames that both live in the shared repo. When another team member does some work and commits their notebook to the shared repo, you can pull changes locally to your computer, open their notebook, select relevant cells, copy and paste them into your own notebook. One simple option with this model is for each group member to create and maintain a subdirectory within the repo where they will stage and modify their own notebooks for their component of the project.
