Question 1:

Which NFL teams have won 3 or more Superbowls?


// SQL CODE USED

select team, count(team) as Wins
from team join teamstats on team.TeamID = teamstats.TeamID
where superbowlwinner = 'Y'
having count(team) >= 3
group by team
order by count(team) desc;
