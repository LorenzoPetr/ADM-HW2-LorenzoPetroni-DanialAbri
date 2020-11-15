# ADM-HW2-LorenzoPetroni-DanialAbri
Git Repository containing the jupyter notebook for ADM's HW2

This repository contains the solution for HW2 provided by the two members of group 22: Lorenzo Petroni and Danial Abri.

This README file was written specifically to provide a key to the contents of the notebook and the results obtained.

Although the code provided is complete, as far as the exercises proposed in the assignment are concerned, 
we have encountered several difficulties in testing the entire code with the complete dataset.
We have tried to set up instances on both AWS-S3 and Google Colab, in both cases without success.
The reasons were many: sometimes due to lack of RAM space on the virtual machine or, more frequently, 
for the time required for execution which always caused a kernel breakdown after hours of runtime.
To try to overcome this problem, we tried to load a different dataset for each assignment, loading each time only the fields we needed to solve the exercise.
However, even in this case, the solution was not sufficient to allow normal execution of all parts of the code.
We found an example of this situation in the code in Exercise 1.3, where we needed all records with event_type = "view" (ie, the vast majority of total records).

So we decided to go like this: for both the October and November datasets we only uploaded 500,000 records, so the aggregate dataset has one million records.
This allowed us to run the code locally without too many problems or slowdowns. 
However, many of the results shown in the notebook will be strongly influenced by this initial choice.
An obvious example can be found in the solution shown for exercise 5.1 in which it is possible to view the average number
of views only for the first two days of the week.
The reason for this is that the complete dataset is sorted according to the event_time field. 
Therefore, by truncating the two datasets both to just 500,000 records, information on the most recent records is lost.
