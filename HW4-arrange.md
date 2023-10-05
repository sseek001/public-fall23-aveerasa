# Homework 4: Arrange Tables

**Due:** Wednesday, October 25, 2023 by 11:59pm  

The goal of this assignment is to propose and implement charts based on questions asked about real-world data.  You will be demonstrating that you can choose and implement charts using appropriate idioms for the data and task, incorporating chart design principles that we have covered.

*Read through the entire assignment before starting.*

## Datasets

Choose **one** of the following datasets. For each dataset, you must address **both** questions using a separate chart for each. You must also discuss the "Further Questions" listed, but you do not need to create charts for that section.

All of the datasets for this assignment come from [Section 2. Births, Deaths, Marriages, and Divorces](https://www.census.gov/library/publications/2009/compendia/statab/129ed/births-deaths-marriages-divorces.html) from the [2010 Statistical Abstract of the United States](https://www.census.gov/library/publications/2009/compendia/statab/129ed.html) (this is different than your HW3 data, which came from the 2012 version).

In addition to looking at the Excel spreadsheets for the Tables listed below, you should also view the [Section 2 PDF](https://www2.census.gov/library/publications/2010/compendia/statab/129ed/tables/vitstat.pdf). 

### Dataset 1

Table 91 - Women Who Have Had a Child in the Last Year by Age

**Q1:** Compare the ages of women at the time of the birth of their first child between 1990-2008. For instance, is there any evidence that women in the US are waiting longer to have their first child?

**Q2:** How does this compare to the number of women in each age group who had a child (not necessarily their first) in that year? What does this say about the age of women giving birth in the US?

**Further Questions:** What further questions does this prompt?  What hypotheses do you have about what the answers might be?  Are there other tables that might help you address these questions?  

**Extra Credit [2 points]:** Combine the data from Tables 91 and 92 (Women Who Have Had a Child in the Last Year By Selected Characteristics) to investigate other factors that affect this.

### Dataset 2

Table 118 - Death Rates for Major Causes of Death--States and Island Areas

**Q1:** Which states had the highest death rates over all causes in 2006?

**Q2:** Is this ordering different if you compare deaths due to disease vs. deaths due to accident, injury, and assault?  In other words, which states are more hazardous to your health vs. which states are the most dangerous?

**Further Questions:** What further questions does this prompt? What hypotheses do you have about what the answers might be?  Are there other tables that might help you address these questions?  

**Extra Credit [2 points]:** Combine this data with the state population distribution by age (found in Table 16 in [Section 1. Population](https://www.census.gov/library/publications/2009/compendia/statab/129ed/population.html)) to investigate other factors that might affect this. (It's ok that the death data is from 2006 and the population data is from 2008 -- it's close enough.)

### Dataset 3

Table 102 - Expectation of Life at Birth, and Projections  
Table 107 - Death Rates by Age, Sex, and Race

**Q1:** Using Table 102, compare life expectancy for people born between 1970-1999 for the four categories, "Male", "Female", "White", "Black".

**Q2:** Using Table 107, compare infant mortality rates (under 1 year) for these same categories between 1980-1999.

**Further Questions:** What further questions does this prompt?  What hypotheses do you have about what the answers might be?  Are there other tables that might help you address these questions?  

**Extra Credit [2 points]:** Combine the data from Tables 102 and 107 to investigate how infant mortality might affect overall life expectancy.

## Assignment

For your chosen dataset, create a chart to answer each of the questions provided. You will be creating two separate charts. *We expect to see variety in the datasets that are chosen.*

As you work through this, pay attention to detail and the visualization principles we have discussed in class when designing your charts.  Charts must have appropriately labeled axes and appropriate unit formats. In your report ([see below](#report)), you will describe the design decisions you have made, so take notes along the way as you work through your design process. 

You may use whatever tool(s) you wish to manipulate the data and create the charts. Remember that CS students must complete at least two HW assignments using Python or Vega-Lite.

**Extra Credit:** In addition to the extra credit available for further exploration of the datasets, there are two other ways to earn extra credit on this assignment:
1. **[4 points]** Re-create the charts you created for your chosen dataset using Python or Vega-Lite.
1. **[5 points]** Complete the full assignment with one of the other datasets.

These are all or nothing -- no partial extra credit given.  You must include a similar writeup for your extra credit charts as for the main assignment.  These guidelines apply also to the extra credit available for further exploration of the datasets.

## Files to Include

Your GitHub repo should contain any files you used to create the charts. This includes smaller datafiles, Excel spreadsheets, Tableau workbooks, Python ipynb notebooks, Python source code, etc. Your repo should also contain images of the created charts so they can be included in your report.

## Report

Your report is an important part of this assignment. It should be written as a narrative and not just a set of bullet points.  Your report should include your name, CS625-HW4, date, and appropriate headings and Markdown markup for clarity and neatness. You will lose points if there are many spelling or grammatical errors. 

Create a section for each question that you are addressing.  Each section must include the following information:

* question you're addressing
* appropriately-sized image of the chart
* link to the chart
    * Excel, Tableau - link to your spreadsheet/workbook in your GitHub repo
    * Vega-Lite - provide a link to your notebook (see ["Note about Using Observable"](#note-about-using-observable) for sharing instructions)
    * Seaborn in Google Colab - provide a link to your notebook (make sure to share with GTA and instructor) or link to your ipynb file in your GitHub repo
    * Seaborn locally - link to your Python code in your GitHub repo
    * other tools - ask if you have questions about what should be submitted
* explanation of how the idiom used in your chart is appropriate for your datasets and question (task)
* idiom/mark/data/encode table (see [markdown code](#markdown-code-for-table) for an example)
* discussion of any design decisions you made
* discussion of any special customizations you used

Your report must also contain the following sections:

* Further Questions - This is where you discuss the further questions prompted by your exploration of the dataset.
* References - This is where you list any resources you consulted.

## Submission

You should be working in the private GitHub repo that was created for you in the odu-cs625-datavis organization. If you are working locally, make sure that you have committed and pushed your local repo, including any images you reference, to GitHub.

Submit the URL of your report (not the URL of your repo) in Canvas under HW4. This should be something like

`https://github.com/odu-cs625-datavis/fall23-mcw-username/blob/main/HW4-report.md` (if you're in Dr. Weigle's class)  
or  
`https://github.com/odu-cs625-datavis/fall23-asv-username/blob/main/HW4-report.md` (if you're in Dr. Veerasamy's class)  

*If you make changes to your report after submitting in Canvas, we will use the last commit time in your repo as your assignment submission time.*

# Appendix

## Markdown Code for Table

Example idiom/mark/data/encode table

Idiom: Bar Chart / Mark: Line
| Data: Attribute | Data: Attribute Type  | Encode: Channel | 
| --- |---| --- |
| state name | key, categorical | vertical spatial region (y-axis) |
| marriage rate | value, quantitative | horizontal position on a common scale (x-axis) |

Markdown code:  
```
Idiom: Bar Chart / Mark: Line
| Data: Attribute | Data: Attribute Type  | Encode: Channel | 
| --- |---| --- |
| state name | key, categorical | vertical spatial region (y-axis) |
| marriage rate | value, quantitative | horizontal position on a common scale (x-axis) |
```

## Note about Using Observable

Once you've been added to the @oducs-vis Observable Team, you can create private notebooks that you can use for your homework assignments.

To create a new private notebook:

* start at https://observablehq.com/@oducs-vis
* click New
* make sure **Workspace** is set to "ODUCS Vis" and **Visibility** is set to "Only You"
* click Create Notebook

To share with your instructor and GTA (for help or for grading):

* click Share
* in the **Search for a teammate** box, enter kgarg001, weiglemc (if you're in Dr. Weigle's class), or ashok-kumar-veerasamy (if you're in Dr. Veerasamy's class)
* choose "Can Edit"
* click Add
* click Save
