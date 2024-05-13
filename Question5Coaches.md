Question 5:

 Return every coach that has won and lost one atleast one Super Bowl.

// SQL CODE USED 

SELECT CoachFirstName || ' ' || CoachLastName AS CoachName, Team,

SUM(CASE WHEN SuperBowlWinner = 'Y' THEN 1 ELSE 0 END) AS SuperBowlWins,

SUM(CASE WHEN SuperBowlWinner = 'N' THEN 1 ELSE 0 END) AS SuperBowlLosses

FROM COACH JOIN TEAMSTATS ON COACH.CoachID = TEAMSTATS.CoachID 

JOIN TEAM ON TEAM.TeamID = TEAMSTATS.TeamID

GROUP BY CoachFirstName, CoachLastName, Team

HAVING SUM(CASE WHEN SuperBowlWinner = 'Y' THEN 1 ELSE 0 END) >= 1 AND

SUM(CASE WHEN SuperBowlWinner = 'N' THEN 1 ELSE 0 END) >= 1

ORDER BY SUM(CASE WHEN SuperBowlWinner = 'Y' THEN 1 ELSE 0 END) DESC;
