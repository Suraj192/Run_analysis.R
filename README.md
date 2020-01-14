# Run_analysis.R
This program script is mandatory assignment for Getting and Cleaning Data 
Program initialize with the loading of program package reshape2 (used for melting and casting data for assignment goal)
Downloading Files from given URL
For the assignment, messed up data was given in the following URL  <- "https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip"
The given data was downloaded and unzipped in the working directory of the R studio.
Code than read the data from the source folder to the R-studio
After the completion of the data reading part, the column than was given the suitable name
Next step was to combine all data set into one dataframe
  in order to do so, at 1st only training data was combined with cbind function
  and then all the test data was combined using similar function
  finally, merging was done between train dataframe and test dataframe with rbind function to form one single
  dataframe called merged
Merged dataframe then passed with the grepl function to match the letter "mean" and "std" throghout the column
similarly, to keep the 1st and second column of data frame we used TRUE fuction
then, all true statement was selected for the required column from merged dataframe.
merged dataframe was then named with the descriptive activity and converted integer form to the factor form with appropriate labelling
Then, merged data was melt with the id 1st and second column
then, molten data was dcast with the variable value mean.
Finally, the tidy data was created in the text format with write.table function
