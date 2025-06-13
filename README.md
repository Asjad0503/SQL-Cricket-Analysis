# SQL-Cricket-Analysis
The IPL 2024 Auction SQL Project: Harnessing Data for Cricket Strategy 🚀
 🌟 Excited to share my SQL project

 The IPL 2024 Auction SQL Project, where SQL takes center stage in transforming complex player data into actionable insights for one of the biggest cricketing events—the IPL Auction.
This project was designed to analyze and manage detailed player profiles, empowering IPL franchises, analysts, and fans with data-driven insights. By leveraging the power of SQL, it bridges the gap between cricket strategies and data analytics.

<h2> Questions and Answers </h2>

1.List all players from India in the auction

select First_Name,Surname,DOB,Country,Age,
Previous_IPLTeam_s,TEAM_2024,reserve_price
from ipl where country = 'India';
