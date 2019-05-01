# Sabermetrics-Project
Final Project for Sabermetrics

Video is showing the code and explaining how everything works!

Fangraphs data is used for this project as well as Lehman data.


_________________________________________________________________
		 	 	 		
								
##  1.1 Explanation of statistic ##
				
As a reminder for my statistic, I decided to calculate when teams begin to lose money on players based off of the contracts they have signed. For my statistic, I evaluated five batters using five important batting statistics SLG, AVG, OBP, and WOBA, I also included WAR to my calculations as overall value for these players. When deciding how to approach this I needed a way to first justify the salary of these players and then determine if as the years went on the players no longer met the justification for these salaries, meaning they no longer played well. So to do this I needed to come up with a point algorithm. So the first thing I did to help visualize where players fall in line with other players is make box and whisker plots and compare players averages to the rest of the league. After getting the plots I then made my point algorithm where each statistic had a weight attached to it where if they scored an average amount of points then they got one point and the points scaled appropriately when the player scored above or below average. When doing this I made WAR have more weight than the other statistics as it serves more overall value for the players. After this was done the points were applied to my five pitchers through several years, starting with the first year they signed their contracts. 

To help explain the point system I created,  we can run through a quick example. Let's say in 2012 the average OBP was 0.1, if a player were to average that same OBP they would get one point. Now if a player got double that OBP they would get two points and so on. This happens for all the statistics expect for WAR, so if a player were to have an average WAR they would get four points, the reason WAR is weighted this way is because I decided that it is as important as the other statistics I am evaluating combined. To see if this point system was working well, I took the average salary for each year and divided that by the point amount an average player would be making, this assigned a monetary value to each point. By doing this I was able to get very close to the players actual salary earnings so I knew that my point system was not far off. 



I then graphed a couple more things. I graphed the players point progression amongst the years as well as the player's actual salary compared to league salary throughout these years for comparison. The reason I did both is to see if the player lost value in terms of performance and then be able to compare that to how much they were making and the rest of the league was making. After this, I used Fibonacci Retracements and applied it to the players point graphs as a replacement level to be able to tell when teams begin to lose money players. Fibonacci retracement uses the golden ratio, which is found naturally in biology and architecture in examples such as logistic population growth, DNA molecular structure, magnetic spins of cobalt molecules, and even the dimensional properties of the Pyramids of Giza. It is a naturally occurring mathematical relationship between two numbers whose ratio is the same as the ratio of their sum to the larger of the two quantities. Algebraically speaking, it can be defined as (a+b)/a = a/b = φ where phi is equal to 1.618. Why is this important? An Italian mathematician named Leonardo Pisano Bigollo, also known as Fibonacci, noticed a relationship between the growing population sizes of rabbits. He noted that the total population of each generation was the sum of the two previous numbers in that sequence, and any number in that sequence divided by the one that precedes it approaches phi, or rather the golden ratio. Today, we use this mathematical relationship to quantify behavior in financial markets through Fibonacci retracements, but this pattern ultimately can be used to find relationships in the forming trends of any sample data set. In traditional technical analysis, the Fibonacci retracement levels are defined at 23.6%, 38.2%, 50%, 61.8%, 78.6% and 100%. All these numbers are derived from different relationships between numbers in the fibonacci sequence. This provides a valuable data point in statistical analysis which is why I have used it to find relationships in player performance versus their monetary value to the team.

For this statistic I decided to focus on the 38.2% line (this level is often used for this technique, I also wanted to hold the players to a higher standard) to be the replacement level of these players, meaning if they dip below this line teams are officially losing money on that player. I also decided because contracts can be very long for some players that if they dip below this line once, it is not enough to say a team is losing money. So with that being said if a player dips below and stays below the 38.2% line for two years or more then a team is then losing money on them. I also graphed the player's salary earnings compared to the MLB average to help see the correlation between performance and salary. 

This statistic is combining multiple stats into one and also considering players worth, which is not being fulfilled by other statistics. It is also providing a unique evaluation method that other MLB stats are not using. This stat fills the need of teams signing these long contracts and not knowing if they are making money off of these players, this helps fill that gap for teams to decide if players performance is worth the money spent. It also can be used as a good way to sign contracts they can see a players performance in the past and see where the dip below lines and make specific contracts that include this stat in it, meaning they can tell a player they will sell them if they dip below the 38.2% line. Teams can also have a contracts opt-out years be based off this statistic as well. A team could also use this stat to see if they are overpaying a player based off their performance by doing the average salary to point matching system. So if a player scored 20 points in a certain year and he is getting paid 20 million but based off of my statistic should only be making 10 million then they know he is getting overpaid for his performance. Overall, it allows teams insight into the true worth of players, so teams know when they are getting good value out players given the money they are spending on them. 
		 	 	 					
				
## 1.2 Demonstration ##


Check the python notebook in the repo to view the statistic and how it works! All graphs are displayed there. 	

When evaluating the statistic make sure to read the graphs and find when players pass the 38.2% line and stay under to see if teams are losing money on that player. 	

If you wanted to test this stat with different players you could change the names of the players when loading in the data :) 

## 1.3 Evaluation of statistic ##
				
			
My statistic compares to other statistics as it takes into consideration players averages and helps teams evaluate players worth kind of like WAR does. When we talk about WAR we have to keep in mind that it is also representing some replacement level if a player reaches 0.0, they are then as valued as someone from the minors, in a way that is what my statistic is doing if a player dips below the 38.2% line. It does differ from such things like WAR as it evaluates players through time and determines their worth through performance. It also has a replacement level that compares the players performance with their very own performance, so teams can measure that individuals performance rather than just comparing to the rest of the league, which is also taking into consideration when calculating the points.



## Possible concerns with my statistic ##

Some concerns with my statistic are the point ranking and the weight system behind it. I feel that if I knew more about baseball and what all these statistics meant for specefic teams the point system could be very accurate, and mine is more general for all teams. I have an understanding of what these statistics are and what they represent, but baseball professionals could find true value in the point rankings. Meaning teams could determine what statistics matter most for them and then weigh things according to that. I also would say the Fibonacci Retracement could be an issue for some MLB teams, as it is not that traditional in sports. I liked using it as it was something unique, new, and nerdy but some folks on an MLB team may not think there is value in it. 


## 1.4 Presentation ## 

Check video in repo!









