Question 2:

What is the average Superbowl point differential categorized by decade? What decade is the highest? Lowest?

// SQL CODE USED 

select round(avg(pointdifference), 0) as AveragePointDifference, case
when SBIndex >= 44 then '2010s'
when SBIndex >= 34 then '2000s'
when SBIndex >= 24 then '1990s'
when SBIndex >= 14 then '1980s'
when SBIndex >= 4 then '1970s'
else '1960s'
end as decade
from superbowl
group by case
when SBIndex >= 44 then '2010s'
when SBIndex >= 34 then '2000s'
when SBIndex >= 24 then '1990s'
when SBIndex >= 14 then '1980s'
when SBIndex >= 4 then '1970s'
else '1960s'
end
order by decade desc;
