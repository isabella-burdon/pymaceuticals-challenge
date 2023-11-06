# pymaceuticals-challenge

Task:

Generate tables (data cleaning and sumary stats)

    (1) Merge mouse_metadata and study_results into a single dataframe
    (2) Display number of unique mouse IDs 
    (3) Check for mouse IDs with duplicate timepoints (using Mouse ID and timepoint):
        - Create a df of duplicates
        - Create a new df with duplicates removed
    (4) Display updated number of unique mouse IDs
    (5) Generate a dataframe of summary stats (using groupby). Include:
        - A row for each drug regimen (with regimen names in the index column)
        - A column for: mean, median, variance, standard deviation, SEM of the tumour volume
    
Generate figures (data visualisation)

    (1) 2 identical barcharts by two different methods.
    Show the total number of rows (Mouse ID/Timepoints) for each drug regimen throughout the study
        - First using: pandas DataFrame.plot()
        - Second using: matplotlib pyplot method
    (2) 2 identical pie charts by two different methods.
    Show the distribution of female versus male mice in the study.
        - First using: pandas DataFrame.plot()
        - Second using: matplotlib pyplot method  
    (3) Generate summary stats for most promising treatment groups and boxplot
        - Generate df with the last timepoint for each mouse (using groupby), merge with cleaned df, reset index, retreive max timepoint for each mouse
        - Generate list with treatment groups: Capomulin, Ramicane, Infubinol, and Ceftamin
        - Generate empty list for tumor volume data, append final tumour volume data (drug, IQR and outliers) with for loop 
        - Generate boxplot with tumour size by treatment regimen
        (https://matplotlib.org/stable/gallery/statistics/boxplot_demo.html)
    (4) Correlation and regression
        - Select a single mouse treated with Capomulin
        - Generate a line plot of tumor volume versus time point for that mouse
        - Calculation the correlation coefficient
        - Calculate the line of best fit (linear regression model)
        - Plot the linear regression model on the scatter plot
    (5) Repeat above for 'the average mouse' treated with Capomulin

Summary of study results

This data is derived from a study of 249 mice with SCC tumours. There are a number of study groups, namely mice are either in the investigational (Capomulin) treatment group or randomised into a number of other standard treatments. There are a total of ten treatment groups. The primary endpoint that is being tested is tumour size.

There were more more mice in the capomulin (230 mice) and Ramicaine (228 mice) compared to other drug regimens, which average 178 mice. There were 51% female and 49% male mice in the study.

A comparison of tumour volume inin a subset of drug regimens found that capomulin and ramincane treated mice had a smaller median tumour volume at 38 and 36 respectively compared to infubinol and caftamin which had a larger median tumour volume of 60 (both). Out of all the medications ramicaine had the lowest median (36) and mean (36) tumour size and capomulin had similar results for its median (38) and mean (37).

A comparison of mouse weight versus average tumour volume in the subset of mice treated with capomulin demonstrated that there was a strong correlation between mouse weight and tumour volume (r = 0.84). Clinical correlation is required to determine if the medication could cause weight loss and is a product of the treatment regimen. It would also be important to ensure that mice have been randomised into the treatment groups appropriately so that mouse size is not biasing the results.

Overal the investigational product seems to be a effective in acheiving the primary endpoint of reducing tumour volume, with similar efficacy to ramicaine, and greater efficacy than all other trialed drug regimens.