Question 3:

Which refs have reffed a team more than once in the Superbowl?

// SQL CODE USED

select refs.reffirstname || ' ' || refs.reflastname as refname, count(team.teamID) as AmountOfTimesReffed, team

from refs join crew on refs.refID = crew.refID

join teamstats on crew.SBIndex = teamstats.SBIndex

join team on teamstats.teamID = team.teamID

group by refs.reffirstname || ' ' || refs.reflastname, team

having count(team.teamID) > 1

order by amountoftimesreffed desc
;
