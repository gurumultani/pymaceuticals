Pymaceuticals Readme file:

# Get all the data for the duplicate Mouse ID
duplicate_mouse_id= merged_data.loc[merged_data.duplicated(subset=['Mouse ID', 'Timepoint']),'Mouse ID'].unique()
duplicate_mouse_id

duplicate_mouse_data = merged_data.loc[merged_data["Mouse ID"] == "g989"]
duplicate_mouse_data

 # Created a clean DataFrame by dropping the duplicate mouse by its ID.
clean_study_data_complete = merged_data[merged_data['Mouse ID'].isin(duplicate_mouse_id)==False]
clean_study_data_complete.head()
-Above codes was written with the help of AskBcs Tutor

# Group the data by 'Drug Regimen' and calculate the total number of timepoints for each drug regimen

timepoints_per_regimen = merged_data['Drug Regimen'].value_counts()

# Generate a bar plot using Pandas
timepoints_per_regimen.plot(kind='bar', ylabel='# of observed Mouse of Timepoints')
plt.show()

-Above code writen with th help of AskBCS Tutor.

- Class Acitivities helped a lot in prepping this challenge especially the last half par; which includes Correlation and Regression, Line plot and scatter plot, Quartiles, finding outliers and also creating a box plot