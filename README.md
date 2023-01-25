# pandas-challenge

Module 4 Challenge
In this assignment, create and manipulate Pandas DataFrames to analyze school and standardized test data and create a short summary of the findings

## Begin the assignment by setting files up for success

- New repository called `pandas-challenge` set up and cloned to my computer and created the folder `PyCitySchools` to work from
- Add Jupyter notebook to this folder for the main script to run for analysis.
- Worked in the assignment a little bit then pushed changes to GitHub.

## Instructions

Report located in the top section of Jupyter Notebook includes a written description of at least two observable trends based on the data.
Using Pandas and Jupyter Notebook, create a report that includes the following data:

### District Summary

Create a high-level snapshot, in a DataFrame, of the district's key metrics, including the following:

- Total schools
- Total students
- Total budget
- Average math score
- Average reading score
- % passing math (the percentage of students who passed math)
- % passing reading (the percentage of students who passed reading)
- % overall passing (the percentage of students who passed math AND reading)

### School Summary

Create a DataFrame that summarizes key metrics about each school, including the following:

- School name
- School type
- Total students
- Total school budget
- Per student budget
- Average math score
- Average reading score
- % passing math (the percentage of students who passed math)
- % passing reading (the percentage of students who passed reading)
- % overall passing (the percentage of students who passed math AND reading)

### Highest-Performing Schools (by % Overall Passing)

Sort the schools by `% Overall Passing` in descending order and display the top 5 rows.
Save the results in a DataFrame called "top_schools" located in the analysis folder in PyCitySchools.

### Lowest-Performing Schools (by % Overall Passing)

Sort the schools by `% Overall Passing` in ascending order and display the top 5 rows.
Save the results in a DataFrame called "bottom_schools" located in the analysis folder in PyCitySchools

### Math Scores by Grade

Perform the necessary calculations to create a DataFrame that lists the average math score for students of each grade level (9th, 10th, 11th, 12th) at each school.

### Reading Scores by Grade

Create a DataFrame that lists the average reading score for students of each grade level (9th, 10th, 11th, 12th) at each school.

### Scores by School Spending

Create a table that breaks down school performance based on average spending ranges (per student).

Use the code provided below to create four bins with reasonable cutoff values to group school spending.
spending_bins = [0, 585, 630, 645, 680]
labels = ["<$585", "$585-630", "$630-645", "$645-680"]
Use `pd.cut` to categorize spending based on the bins.

Use the following code to then calculate mean scores per spending range.
spending_math_scores = school_spending_df.groupby(["Spending Ranges (Per Student)"]).mean()["Average Math Score"]
spending_reading_scores = school_spending_df.groupby(["Spending Ranges (Per Student)"]).mean()["Average Reading Score"]
spending_passing_math = school_spending_df.groupby(["Spending Ranges (Per Student)"]).mean()["% Passing Math"]
spending_passing_reading = school_spending_df.groupby(["Spending Ranges (Per Student)"]).mean()["% Passing Reading"]
overall_passing_spending = school_spending_df.groupby(["Spending Ranges (Per Student)"]).mean()["% Overall Passing"]

Use the scores above to create a DataFrame called `spending_summary`.

Include the following metrics in the table:
-Average math score
-Average reading score
-% passing math (the percentage of students who passed math)
-% passing reading (the percentage of students who passed reading)
-% overall passing (the percentage of students who passed math AND reading)

### Scores by School Size

Use the following code to bin the per_school_summary.
size_bins = [0, 1000, 2000, 5000]
labels = ["Small (<1000)", "Medium (1000-2000)", "Large (2000-5000)"]
Use `pd.cut` on the "Total Students" column of the `per_school_summary` DataFrame.

Create a DataFrame called `size_summary` that breaks down school performance based on school size (small, medium, or large).

### Scores by School Type

Use the `per_school_summary` DataFrame from the previous step to create a new DataFrame called `type_summary`.
This new DataFrame should show school performance based on the "School Type".

# Short summary of the analysis

In this analysis, overall, Charter schools had higher grades. From this analysis we are unable to determine why this is the case. Generally the feeling is that these schools are smaller in class size therefore our young humans tend to receive more individualized coaching with their studies. However, this data could also simply be victim to a large number of highly intelligent, motivated human teenagers going to school at this time. When analyzing the data by the size of school we find a similar trend if making the assumption of smaller class sizes. The overall passing scores were a little higher at the medium school level where there could be additional challenges for the students and possibly more individualized resources contributing to their learning experience. Again, could simply be a large number of very smart people working their way to adulthood. Spending ranges per student brings about an interesting study. With the increased amount of spending per student, we would be inclined to think these resources would propel our young into having the resources to earn better grades. Perhaps a study into how this money is spent so as to understand the impact this has on the student scores would be in order. Looking at the scores for each school, comparing them, overall, the schools are experiencing around the same scores by grade. The reading grades are pretty close but the math grades show a wider variance. Without digging into each school's plan of action in the process and the impact of their processes, it is difficult to determine why this is. The top and bottom performing schools show a small variance among their respective groups. The top performers do have less students. Again, further analysis would be required to find out why. Statistics alone don't tell enough of the story. Overall, reading scores have less of a variance. The data doesn't tell us why but this is good news for our young humans moving into the future and great news for us as we age. I take comfort in knowing that the person who delivers medicine to me in the future will likely be able to read the precautions and understand the implications if my chart has an allergy listed, I just worry about the dose calculations.
