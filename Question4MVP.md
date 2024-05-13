Question 4:

Return every Superbowl MVP that was not a quarterback

// SQL CODE USED 

SELECT PLAYER.PlayerFirstName || ' ' || PLAYER.PlayerLastName AS PlayerName, Position

FROM PLAYER JOIN PLAYERSTATS ON PLAYER.PlayerID = PLAYERSTATS.PlayerID

WHERE Position <> 'QB' AND MVP = 'Y';
