Project Guidelines
=======
There are five main blocks of codes in run_analysis.R

1. Loading the data from the working directory by using read.table(), for both the test and train datasets, along with the descriptive datasets "features", "subject test" and "activity labels"
2. Putting everything together for each of the test and train datasets - adding the column names, filtering for just the columns calculating the mean and standaard deviation of the variables (It's questionable whether to include "Freqmean." I leave them for the completeness of the data.)
3. Combining the two datasets with rbind() - stacking them on top of each other (both have same number of variables and names). The two dataset by design does not share SubjectIDs so no need to merge
4. Melting the dataset using sujectID and activity as IDs, the rest of the columns as variables. Then dcast(), joining the two ids and calcualte the mean for each unique combination. 
5. Export the data to a txt file using write.table

I believe the original features.txt is self-explainatory and there is no need to rename the variables in features to give a more descriptive name. 
