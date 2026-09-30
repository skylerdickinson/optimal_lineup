# MLB Optimal Batting Lineup Model - Texas Rangers 

This is one of my projects I had completed in the spring semester of 2026!  
A mixed-integer optimization model that builds the best possible batting lineup and defensive alignment for the Texas Rangers against right-handed and left-handed pitchers.  

Found the data from FanGraphs.com and focused on the Texas Rangers.

Looked at the players who had more than 100 plate appearances over seasons 2022-2025 to have a sizeable player pool to optimize results further.  
To populate parameter values in the model, I used wOBA, split wOBA, OBP, SLG, wRC+, BB, L/R handed, defensive WAR per 162, as well as a players primary and secondary positions at defense. 

Was able to build an optimal lineup for both LHP’s and RHP’s using these player specific statistics.    

## What it does
- Blends each player's overall wOBA with their platoon splits (vs RHP / LHP), weighted by plate appearances. 
- Accounts for batting order position, defensive value by position, and on-base/power pairing.
- Solves for the optimal lineup using Pyomo and HiGHS solver.

## Files
- "FinalModel.ipynb": the model and results
- "FinalModelBreakdown.ipynb": same as FinalModel.ipynb but has more of a breakdown of results
- "rangers_lineup_data_new.xlsx": player stats used as input.

## How to run
- Install packages: 'pip install pyomo highspy openpyxl pandas'
- Open "FinalModel.ipynb" and run all cells

## Author 
Skyler Dickinson
