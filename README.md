# Matplotlib-challenge : Pymaceuticals Inc.
I analized data obtained by the pharmaceutical company Pymaceuticals, Inc. for potential treatments for squamous cell carcinoma (SCC). I analyzed their results treating 249 mice with SCC tumors that received different drug treatments over the course of 45 days. 

1. First, I imported the data provided in two csv files, `mouse_metadata.csv` and `study_results.csv`. I stored the data into one pandas dataframe.

2. I used `len()` to get the number of mice in the dataset, there were `249` mice. I used `duplicated()` to find the mouse ID of duplicate mice, `g989` was duplicate, and removed the duplicate mouse in order to clean up the dataset.

![alt text](https://github.com/glongo001/matplotlib-challenge/blob/main/Pymaceuticals/Images/clean_study_data.png)

3. I created a table displying summary statistics, such as mean tumor volume, median tumor volume, tumor volume variance, tumor volume standard deviation, and tumor volume standard error.
    - The results of this table implied that Capomulin and Ramicane were the most effective treatments.

    ![alt text](https://github.com/glongo001/matplotlib-challenge/blob/main/Pymaceuticals/Images/summary_stats.png)

4. I obtained the number of mice treated with each drug regimen and displayed the results in a bar graph. 
    - I created a bar graph with pandas:

    ![alt text](https://github.com/glongo001/matplotlib-challenge/blob/main/Pymaceuticals/Images/bar_pandas.png)

    - I also created a bar graph with pyplot:

    ![alt text](https://github.com/glongo001/matplotlib-challenge/blob/main/Pymaceuticals/Images/bar_pyplot.png)

    - I discovered that more mice were treated with `Capomulin` and `Ramicane`, 230 and 288 respectively, less than 190 mice were treated with all the other treatments.

5. I obtained the number of male and female mice treated and displayed the results in a pie chart. 51% of mice treated were male and 49% of mice treated were female.
    - I created the pie chart with pandas:

    ![alt text](https://github.com/glongo001/matplotlib-challenge/blob/main/Pymaceuticals/Images/pie_pandas.png)

    - I also created the pie chart with pyplot:

    ![alt text](https://github.com/glongo001/matplotlib-challenge/blob/main/Pymaceuticals/Images/pie_pyplot.png)

6. I separated the data of the top 4 performing regimens: `Capomulin`, `Ramicane`, `Infubinol` and `Ceftamin`. I used `max()` to obtain data from the maximum timepoint for each mouse and kept the final tumor volume in mm3 for each mouse. I obtained the quartiles (25%, 50%, and 75%) for the final tumor volume and calculated the upper and lower bounds to determine outliers. Only `Infubinol` had an outlier with a final tumor volume of 36.3 mm3. I displayed the final tumor volume for each of these treatments in a boxplot, here Capomulin and Ramicane showed lower final Tumor Volumes than Infubinol and Ceftamin.

![alt text](https://github.com/glongo001/matplotlib-challenge/blob/main/Pymaceuticals/Images/boxplot.png)

7. I displayed the tumor volume of mouse `I509` treated with `Capomulin` over time. The results showed that tumor volume decreased over time.

![alt text](https://github.com/glongo001/matplotlib-challenge/blob/main/Pymaceuticals/Images/lineplot.png)

8. I displayed the weight and average tumor volume of mice treated with `Capomulin`.

    ![alt text](https://github.com/glongo001/matplotlib-challenge/blob/main/Pymaceuticals/Images/scatterplot.png)

    - There was a strong correlation showing that as weight increased average tumor volume increased, the correlation was 0.71.

    ![alt text](https://github.com/glongo001/matplotlib-challenge/blob/main/Pymaceuticals/Images/scatterplot_lr.png)

### Analysis
- The summary table shows that Capomulin and Ramicane have the lowest mean tumor volume, the lowest median, the lowest variance, the lowest standard deviation, and the lowest standard error across all timepoints. This data implies that these two drug treatments were the most effective.
- More mice were treated with Capomulin and Ramicane, 230 and 228 respectively, while between 145 and 190 mice were treated with all other drugs. Capomulin and Ramicane treated larger populations while maintaining the lowest medians, variance and standard deviation, implying that they must have been the most effective treatments.
- When comparing the top 4 performing drug treatments Capomulin and Ramicane showed a lower final tumor volume than Infubinol and Ceftamin, confirming that they must have been the most effective treatments.
- When looking at the tumor volume of a mouse treated with Capomulin over time it is clear that tumor size decreases as treatment continues.
- When looking at the average tumor volume and weight of mice treated with Capomulin there is a strong correlation showing that as tumor volume increases mouse weight is greater.
