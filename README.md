# Election_Analysis
## Overview of Election Audit
Tom, a Colorado Board of Elections employee has given me the following tasks to complete the election audit of a recent local congressional election.

1. Reporting the total number of votes cast.
2. Get a complete list of candidates who received votes.
3. Calculate the total number of votes each candidate won.
4. Calculate the percentage of votes each candidate won.
5. Determine the winner of the election based on popular vote

Additionally, the election commission has requested some additional data to complete the audit:

1. The voter turnout for each county
2. The percentage of votes from each county out of the total count
3. The county with the highest turnout

The python code created will automatically determine the winner of the election by counting the number of votes, identifying the different candidates and counties, and calculating the number and percentage of votes for each candidate and county. As a result of using this code, the Board of Elections will save time from execution and reduce human errors by avoiding to manually enter formulas in excel.

## Resources 
- Data Source: election_results.csv
- Software: Python 3.7.6, Visual Studio Code 1.53.2

## Election-Audit Results
The code's summary output of the election is shown below:

![Summary_Results](Summary_Results.PNG)

According to the analysis of the election:
* There were 369,711 votes cast in the election.
* The counties that participated in the congressional election were:
    - Jefferson
    - Denver
    - Arapahoe 
 
    Their respective election results are the following:

    ![Counties_Election_Results](Counties_Election_Results.PNG)

* The county with the largest number of votes was Denver, with a 82.8% of the total votes
* There were three candidates in the election and they were:
    - Charles Casper Stockham
    - Diana DeGette
    - Raymon Anthony Doane
* The candidate results were the following:
    
    ![Candidates_Election_Results](Candidates_Election_Results.PNG)

* The winner of the election was:
    - Diana DeGette, who received 73.8% of the total votes and 272,892 number of votes. 

## Election-Audit Summary

The purpose of this code is to automatically determine the winner of the election by counting the total number of votes, identifying the candidates and the counties in an election, and calculating their respective votes and percentages. 

The election commission could use this code not only for other future U.S. Congressional districts elections but also for senatorial districts and local elections. Before automating this process using this code, this job was normally done in excel which is prone to human error and takes longer time to execute and review, especially when the dataset gets larger. By using this code, it is possible to instantly determine the candidates in an election, counting their votes and calculating their percentages of the votes without any errors and regardless of the size of the dataset.

One way this code can be modified for future use is by specifiying which file to read from and the name of the text file to write on. This will allow the election board to use any future election results cvs files that are structured in a similar fashion. In this code, the part that needs to be modified will be the part as shown in the image below. With the "os.path.join" method, the users of the code would not have to provide the specific path of the csv file, but would only have to list the name of the folder and then the name of the csv file. Similarly, the user will have to specify the folder name and the name of the text file that the code will be writing on. By learning how to select which files to read from and where to export the output to, users of the code would be able to easily determine the results of this election with minimal modification to the code.

![File_Names_To_Change](File_Names_To_Change.PNG)

Another way this script could be adapted for broader elections such as the senatorial election is by adding more layers into which the information could be filtered. This method will request much more modifications to the current code but could provide more insights than the current code. For instance, in a senatorial election, it would be helpful to not only show the election results in a local county-level but also show the information in cities or towns levels. This information would be helpful in seeing the popular vote composition in a local level and predicting future elections. Nevertheless, depending on the state, the code has to be adjusted depending on the governmental system in each state, since not all states have the same composition. For instance, the entire local government exists at the local township level in Massachussetts or in Virginia where cities are completely separate entities from counties. The code will be adjusted according to how granular the data provided is. Depending on the granularity of the data, new lists and dictionaries will be created to store the data and for loops will also be created to organize the data. As a result of these adjustments to the code, more insights can be extracted from the data which would be helpful for future elections.