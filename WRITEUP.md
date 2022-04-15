For the first visualization, I wanted to graph the relationship between a the number of yards a wide receiver had during his best college season and his highest PFF grade as a pro. You could not see the relationship between the data in the graph just by looking at the data since there are multiple position groups within the data, and you cannot sort the tables by the two columns at once. 

This visualization was difficult to create because I had to find the best grade for each player for a season where they played at least 200 snaps at receiver. To do this, I took the following steps:

- Filter out players who didn't have college stats
- I had to find which column had their max grade and find the year they had their best grade in, and put both of those values in new columns
- Use sed to rename the values for the year that they had their best grade in so I could find the amount of snaps they had in that year
- I then had top run a list comprehension on the rows to find the values, and filter out grades that were earned without 200 snaps

Then I could finally use altair to graph the relationship. The results were not as conclusive as I would've liked, but I used an encoding to see that the outliers for receivers that were at the top left of the graph were exemplary players. I also realized that there were fewer players that fell into that category, and the data has a slight linearly increasing trend. It may have been helpful to run a linear regression on the data. There was not a strong correlation for HBs, and a very weak one for TEs.

I did a scatter plot so I could see each individuals position in the relationship and look at density to see if there is a correlation between the two statistics.

For my second visualization, I wanted to see if I could find proof behind the common idea that the NFL is becoming more of a passing league by finding the change of the average grade for QBs, RBS, and WRs. Looking back, it may have been better to find the relationship between how yards are gained. It also may be helpful to have defensive grades to determine this visualization as well to see if defenses are defending the run or pass better in different years.

For this visualization, it was very difficult to make a table, so after a long time struggling to look through Pandas documentation, I decided just to use python loops to parse the data. The reason I had this problem is because I wanted to keep all rows, but I wanted to nnullify data for grade columns for corresponding snap count columns. This is because I didn't want to include data from years where a player did not have a substantial amount of snaps to prevent bias. I think I could've done some sort of iteration with loc, but I couldn;t figure out how to do that. But the python loops ended up working out.

This visualization shows that quarterbacks have been performing better in recent years, while receivers have been mostly constant. Runningbacks had a dip in performance in 2015 and 2016 which is very interesting, but on average, they also have a constant regression. This graph does not prove that runningbacks are performing worse like I would have hoped with my hypothesis, but it is clear that quarterbacks are performing at a very high level. 

It would have been more interesting if I could get data from the past 30 years, but PFF was not started until 2004. It would be interesting to get data from then though, but that would've taken a lot of time to download all of those tables and build the new comprehensive player tables. But, that may be something I should do for my final project.

I did a line graph because I am showing data over time, and the different colored lines lets me easily compare performance between position groups on the same graph.
