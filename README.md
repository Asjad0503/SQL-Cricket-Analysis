# SQL-Cricket-Analysis
The IPL 2024 Auction SQL Project: Harnessing Data for Cricket Strategy 🚀
 🌟 Excited to share my SQL project

 The IPL 2024 Auction SQL Project, where SQL takes center stage in transforming complex player data into actionable insights for one of the biggest cricketing events—the IPL Auction.
This project was designed to analyze and manage detailed player profiles, empowering IPL franchises, analysts, and fans with data-driven insights. By leveraging the power of SQL, it bridges the gap between cricket strategies and data analytics.

<h2> Questions and Answers </h2>

1.List all players from India in the auction?

select First_Name,Surname,DOB,Country,Age,
Previous_IPLTeam_s,TEAM_2024,reserve_price
from ipl where country = 'India';

2.Find players with a reserve price above 150 Lakhs?

select First_Name,Surname,DOB,Country,Age,
Previous_IPLTeam_s,TEAM_2024,reserve_price
 from ipl   where reserve_price >=  150;

 3. Get the names of players who represented "RCB" in 2024?

select First_Name,Surname,DOB,Country,Age,
 Previous_IPLTeam_s,TEAM_2024,reserve_price,C_U_A
 from ipl where TEAM_2024 = 'RCB';

 4. Identify the oldest player in the auction?
    
  select First_Name,Surname,DOB,Country,Age
 from ipl order by Age desc;

 5. List all players along with the difference in their reserve price and the average reserve price?
    
 select First_Name,surname,Country,DOB,TEAM_2024,reserve_price,
  reserve_price - (select AVG(reserve_price) from ipl) 
  as avg_reserve_price from ipl;

  6. Find players who have played more than 50 ipl matches?
 
   select First_Name,Surname,DOB,Country,Age,
	Previous_IPLTeam_s,TEAM_2024,reserve_price,C_U_A,IPL
 from ipl where IPL >50;

8. List all players who have been part of more than one IPL team?

   select First_Name,Surname,DOB,Country,Age,Previous_IPLTeam_s,
   TEAM_2024,reserve_price,C_U_A
 from ipl where Previous_IPLTeam_s  like '%,%';

8. Retrieve players who are both batters and bowlers (dual specialism)?

   select First_Name,Surname,Previous_IPLTeam_s,Specialism,Orientation_Batting,
   Orientation_Bowling TEAM_2024,reserve_price,C_U_A
 from ipl where Specialism = 'all-rounder';

9. Find players who are younger than 30 years old and have a reserve price above 100 Lakhs?
   
 select First_Name,Surname,DOB,Country,Age,
 Previous_IPLTeam_s,TEAM_2024,reserve_price
 from ipl  where Age < 30 and reserve_price > 100;

 10. Retrieve the total number of players per country participating in the auction?

 select count(*) as total,country from ipl
 group by country
 order by total desc;

