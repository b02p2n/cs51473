java c
Fall 2024 CS 17700 — Lab 06 
Submission files:  lab06.py
Submission deadline: Monday November 11 @ 11:59 PM
Late deadline: Thursday November 14 @ 11:59 PM (–20% penalty)
Attempts:  10
All times are local to the Purdue West Lafayette campus (Eastern Time) 
Objectives: 
•   Implement functions based on design criteria
•   Read formatted data from a file
•   Analyze and visualize data through plotting
Description: The Union of European Football Associations (UEFA) would like some insight into the performance of the teams that compete in its Champions League competition. Your Python program will analyze score information from a season of games to determine the winners of each game and the season performance of each team.
Task 1: Game time (20% of grade)
•   Add import matplotlib.pyplot as plt to the top of your lab06.py file.
•   Create a function called load_games which accepts a single required positional parameter named filename (str).
o Use the open() function and a for loop to read the contents of the file line-by-line.
o The file is in comma-separated value format (CSV). The meaning and data type of each column of values is the following:
Team 1 name,Team 2 name,Team 1 score,Team 2 score
str                ,str               ,int               ,int
o Your function should build and return a 2D list, where each sub-list contains the data for a particular game.
[[Team 1 name, Team 2 name, Team 1 score, Team 2 score], ...]o Warning: you are not permitted to import the csv library; this will earn a score of zero.
•   Your workarea in Vocareum contains several CSV files which will be used to test your program. See the end of this handout for more information on the CSV files.
Example execution 1: (not all lines shown)
>>> load_games ("s_sample.csv")
[['Chelsea', 'Inter Milan', 1, 0],
['Arsenal', 'Liverpool', 3, 5],
['Liverpool', 'Arsenal', 1, 0],
['Inter Milan', 'PSG', 3, 5],
['PSG', 'Juventus', 1, 1],
['AC Milan', 'Inter Milan', 3, 5],
['Barcelona', 'PSG', 3, 0],
['AC Milan', 'Liverpool', 4, 0],
['Chelsea', 'Borussia Dortmund', 1, 4],
['Inter Milan', 'Borussia Dortmund', 4, 5],
...]
Task 2: Team report cards (35% of grade)
•   Create a function called grade_teams which accepts a single required positional parameter: games (the 2D list produced by your load_games function from Task 1).
o For each game, the winning team will be the team with the higher score.
o In the event of a tie (a game in which both teams end with the same score), there is no winner.
o Your function should build and return a dictionary where the keys are the names of all  teams, and the values are a list of two integers: the total number of goals scored by that team during the season, and the total number of games won by that team during the season.
{Team name: [Total goals, Total games won], ...}
•    Some example executions are provided below. The auto-grader may perform. additional tests with other data.
Example execution 2: 
>>> grade_teams(g代 写CS 17700 — Lab 06 Fall 2024Python
代做程序编程语言ames) # from s_sample.csv
{'Chelsea': [10, 2],
'Inter Milan': [31, 2],
'Arsenal': [19, 2],
'Liverpool': [17, 3],
'PSG': [12, 3],
'Juventus': [20, 4],
'AC Milan': [31, 6],
'Barcelona': [29, 4],
'Borussia Dortmund': [23, 4],
'Atletico Madrid': [15, 3],
'Real Madrid': [16, 2],
'Manchester City': [16, 4],
'Bayern Munich': [18, 2]}
Task 3: Plotting (45% of grade)
•   Create a function called plot_goals which accepts a single required positional parameter: report_card (the dictionary produced by your grade_teams function from Task 2).
o Your function will make a bar chart that displays the total number of goals scored by each team during the season.
o The x-axis label is "Teams".
o The y-axis label is "Goals".
o For the x-axis values, use the first three letters of each team name converted to uppercase.
o Hint: use the function call plt.xticks(rotation=-45) to rotate the x-axis labels by –45º degrees. Place a plt.tight_layout() function call immediately before saving and showing the plot. This will ensure that all team name abbreviations are legible. 
o Note: the auto-grader requires that you save the resulting plot to a PNG file named o_goals.png. Add a call to plt.savefig("o_goals.png") immediately before using the plt.show() function call.
•    Some example executions are provided below. The auto-grader may perform. additional tests with other data.
Example execution 3: 
>>> plot_goals (report_card) # from s_sample.csv
o_goals.png 

Policies: 
• Review the syllabus for policies regarding extensions and academic integrity. 
•   All submissions must be made through Vocareum. No work will be accepted via any other method.
•   Your code must be placed into a file named lab06.py inside of the work/ folder in Vocareum. No variation is permitted.
•   You may make up to 10 submissions. Each submission will produce feedback from the auto-grader.
•   Your auto-grader score in Vocareum for your last submission is final.
•   You may make a private post on Ed if you believe your assignment was incorrectly scored by the auto- grader. This must be done within 5 days of the score entering the Brightspace gradebook.
Unit testing: Please refer to the Lab 04 handout for more information on how your work will be graded.
• DO NOT CALL input() or print()ANYWHERE except inside the   main   block (if any). Notes on CSV files: 
•   You do not need to edit these files unless it is useful while developing your solution. Do not edit the CSV files with Microsoft Excel as this will change their format and potentially break your code.
•   It is not recommended to make any changes to the CSV files within Vocareum — any such changes will be reset upon each submission.
•   Instead, it is recommended that you download all provided CSV files from Vocareum to your computer  so that you may test your solution with Spyder. Make sure the CSV files are saved to the same folder as your .py solution file.







         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
