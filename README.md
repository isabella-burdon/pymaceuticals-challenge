# pymaceuticals-challenge

Study details:
- Sample: 249 mice with SCC tumours
- Study groups: 
    (A) Investigational (Capomulin) treatment group
    (B) Other standard treatments
- Methods: 45 days of observation, measurement of tumour volume
- End points: tumour volume

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