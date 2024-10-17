# Manchester City Performance Analysis 2022/2023

## Objective:

Analyze the performance of Manchester City during the 2022/2023 season across various metrics, including attacking performance, defensive actions, and trends over the season. This analysis will explore both individual player contributions and overall team performance using data from various competitions.

## Subtasks:

### 1. **Attacking Metrics Analysis**
   - **Description**: Evaluate the attacking performance of players by analyzing goals (GF) and expected goals (xG) during the season.
   - **Data Used**: Columns `Rendimiento_Gls.`, `Expectativa_xG`
   - **Visualization**: Scatter plot showing the correlation between goals scored and expected goals (xG), with player images displayed at their respective data points.
   - **Code**: Used `matplotlib`, `OffsetImage`, and `mplsoccer` to create a visually appealing plot.
   
   ![example_image](images/scatter_goals_xg.png)

### 2. **Home vs Away Performance**
   - **Description**: Compare Manchester City's performance when playing at home versus away, focusing on metrics such as goals scored, goals conceded, and expected goals (xG).
   - **Data Used**: Columns `GF`, `GC`, `xG`, `xGA`, `Sedes` (Home/Away)
   - **Visualization**: Bar chart comparing goals, expected goals, and goals conceded for home and away matches.

### 3. **Defensive Metrics by Player Position**
   - **Description**: Analyze how defensive contributions (tackles, blocks, interceptions) vary across different player positions (e.g., Defenders, Midfielders, Attackers).
   - **Data Used**: Columns `Posc`, `Derribos_Tkl`, `Bloqueos_Bloqueos`, `Int`
   - **Visualization**: Stacked bar chart showing defensive actions per position.

### 4. **Key Players Defensive Comparison**
   - **Description**: Compare the defensive contributions of key players such as Rodri, Rúben Dias, Kyle Walker, and John Stones in terms of tackles, blocks, and interceptions.
   - **Data Used**: Columns `Jugador`, `Derribos_Tkl`, `Bloqueos_Bloqueos`, `Int`, `Err`
   - **Visualization**: Bar chart comparing key defensive metrics for selected players.

### 5. **Effectiveness in Defensive Duels**
   - **Description**: Analyze the effectiveness of players in defensive duels, comparing the percentage of successful tackles (`Tkl%`) and the number of duels attempted.
   - **Data Used**: Columns `Jugador`, `Desafíos_Tkl%`, `Desafíos_Att`
   - **Visualization**: Scatter plot showing duel attempts vs. percentage of successful tackles, with the size of the points representing the number of duels.

### 6. **Defensive Contributions per 90 Minutes**
   - **Description**: Normalize defensive metrics per 90 minutes to provide a fair comparison of players who played different amounts of time during the season.
   - **Data Used**: Columns `Jugador`, `Derribos_Tkl`, `Bloqueos_Bloqueos`, `Int`, `90 s`
   - **Visualization**: Bar chart comparing defensive metrics (tackles, blocks, interceptions) per 90 minutes for each player.

### 7. **Defensive Actions Across Different Zones**
   - **Description**: Analyze where most of the defensive actions (tackles, blocks, interceptions) occur on the field — in the defensive, central, or attacking thirds.
   - **Data Used**: Columns `Derribos_3.º def.`, `Derribos_3.º cent.`, `Derribos_3.º ataq.`
   - **Visualization**: Stacked bar chart showing defensive actions per third of the field.

### 8. **Errors and Ball Losses Analysis**
   - **Description**: Investigate which players are more prone to making defensive errors and losing challenges during the season.
   - **Data Used**: Columns `Jugador`, `Err`, `Desafíos_Pérdida`
   - **Visualization**: Bar chart showing the number of defensive errors and lost challenges per player.

---

## Tools Used:

- **Pandas**: For data parsing and analysis.
- **Matplotlib**: For creating various visualizations, including scatter plots and bar charts.
- **mplsoccer**: For generating soccer-specific visualizations, including player positioning and heatmaps.
- **difflib**: To match player names with image files.
- **PIL**: To manipulate and display player images in the plots.

---

## Running the Analysis:

To replicate this analysis, follow these steps:

1. **Install the required packages**:
   ```
   pip install pandas matplotlib mplsoccer pillow difflib
   ```
2. **Download the datasets**: Ensure the datasets from FBref and Understat are properly loaded into the script.
3. **Run the Python script**: The visualizations will be generated and saved to the `images/` directory.

---

## Conclusion:

This project demonstrates how various metrics, both defensive and offensive, can be analyzed to provide insights into Manchester City’s performance during the 2022/2023 season. The visualizations and statistical analyses highlight key trends and player performances, providing an in-depth look into the team’s tactics and efficiency.
