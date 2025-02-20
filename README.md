# F1 2024 Season Analysis EDA Project

## Overview
This project conducts an exploratory data analysis (EDA) of the 2024 Formula 1 season, leveraging the `fastf1` Python library to fetch, process, and analyze race data, including lap times, tire strategies, driver performances, and qualifying battles. The analysis focuses on key metrics such as race finishes, qualifying positions, lap performance trends, teammate battles, and track-specific driver strengths across all 24 Grand Prix events of the season. Additionally, the project closely examines pole lap comparisons for the top 2 drivers in each round, analyzing speed, throttle, time delta, and sector-wise performance. The project aims to uncover insights into driver consistency, race and qualifying strategies, and team performance on various circuits.

## Purpose
The primary objective is to perform a comprehensive analysis of the 2024 F1 season to identify patterns, trends, and standout performances among drivers and teams. This includes evaluating lap performances, tire strategies, driver consistency, teammate competitions, track-specific strengths, and detailed pole lap comparisons to highlight competitive edges and strategic nuances.

## Dependencies
To run this project, you need the following Python libraries installed:
- `fastf1` (for F1 data access and processing)
- `pandas` (for data manipulation and analysis)
- `numpy` (for numerical computations)
- `matplotlib` (for static plotting)
- `seaborn` (for enhanced data visualization)
- `plotly` (for interactive visualizations)

## Installation
1. Clone this repository or download the notebook and data files.
2. Create a virtual environment (optional but recommended):
   ```bash
   python -m venv myenv
   source myenv/bin/activate  # On Windows: myenv\Scripts\activate
   ```
3. Install the required dependencies:
   ```bash
   pip install fastf1 pandas numpy matplotlib seaborn plotly
   ```
4. Ensure you have a stable internet connection, as `fastf1` fetches data from the F1 API and caches it locally for performance (a `cache` directory is created automatically).

## Usage
1. Open the Jupyter notebook (`F1_2024_Season_Analysis.ipynb`) in a Jupyter environment (e.g., Jupyter Notebook or JupyterLab).
2. Run the cells sequentially to load the data, process it, and generate visualizations and insights.
3. The notebook uses cached data to improve performance, so ensure the `cache` directory is accessible and not deleted during analysis.
4. Modify the `round_numbers` or `track_names` as needed to focus on specific races, drivers, or tracks.

## Project Structure
- `F1_2024_Season_Analysis.ipynb`: The main Jupyter notebook containing the code, data loading, analysis functions, and visualizations.
- `cache/`: Directory for storing cached F1 data to speed up subsequent runs.
- `README.md`: This file, providing project documentation and instructions.

## Key Functions and Analyses
- `get_driver_standings()`: Fetches and aggregates driver standings (points and positions) for each race round.
- `get_quali_battles()`: Compares qualifying positions between teammates for each race, analyzing performance gaps and consistency within teams.
- `get_track_specific_strengths()`: Identifies drivers’ and teams’ performance strengths on specific tracks, based on race and qualifying results.
- Teammate battles: Compares qualifying and race finish positions for drivers within the same team (e.g., Red Bull, Ferrari, Mercedes, etc.).
- Lap performance and tire strategies: Analyzes top 3 finishers per race for consistent lap times, pit stop patterns, and tire compound usage.
- Pole Lap Comparison: Detailed analysis of the pole lap for the top 2 drivers in each round, comparing speed, throttle, time delta, and sector-wise performance to determine competitive advantages.

## Key Findings
### Lap Performance and Tire Strategies (Top 3 Finishers)
- **Consistent Lap Times with Pit Stops:** Across most races (e.g., Bahrain, Las Vegas, Abu Dhabi), top drivers maintain consistent lap times (e.g., 90–110 seconds) with spikes during pit stops, typically indicating two-stop strategies.
- **Tire Strategy Trends:** Medium tires (yellow) are predominantly used for longer stints (10–30 laps), while Hard (white) or Soft (red) tires are used for shorter stints, reflecting a balance of pace and durability.
- **Close Competition Post-Pits:** Top drivers (e.g., VER, NOR, LEC) show tight competition after pit stops, suggesting effective tire management and strategic execution.

### Pole Lap Comparison
- **Speed and Throttle Analysis:** The top 2 drivers in each qualifying session (e.g., VER and NOR in Bahrain) show differences in speed and throttle usage, with faster drivers often maintaining higher average speeds and optimized throttle control through key sectors.
- **Time Delta Insights:** Time deltas between pole setters and second-place qualifiers reveal critical moments where one driver gains or loses time, often in specific sectors (e.g., VER’s slight edge over SAI in Bahrain).
- **Sector-Wise Performance:** Sector comparisons highlight which driver excels in fast, medium, or slow sectors, such as NOR outperforming LEC in Sector 1 of the Monaco GP, or VER dominating Sector 3 in high-speed tracks like Monza.

### Driver Consistency
- **High Variability:** Drivers like Verstappen (VER), Hamilton (HAM), Norris (NOR), and Leclerc (LEC) show high standard deviations in performance, reflecting podium potential but also vulnerability to DNFs or poor results.
- **Low Variability:** Drivers like Bottas (BOT), Sargeant (SAR), and Zhou (ZHO) exhibit lower variability, often finishing consistently low or out of points.

### Teammate Performance
- **Red Bull Racing:** Verstappen dominates Perez consistently, with Perez showing significant inconsistency (e.g., low finishes in Australia, Qatar).
- **Ferrari:** Leclerc and Sainz are closely matched, with Leclerc showing slight consistency, while Sainz struggles in some races (e.g., Singapore).
- **Mercedes:** Hamilton and Russell have a close but variable battle, with Russell gaining momentum late in the season.
- **McLaren:** Norris and Piastri are highly competitive, with Piastri improving over time, though Norris won the Abu Dhabi GP.
- **Aston Martin:** Alonso is more consistent than Stroll, who shows variability and occasional strong mid-season performances.
- **Kick Sauber:** Bottas and Zhou show dynamic competition with neither dominating, both displaying inconsistent finishes.
- **Haas:** Hulkenberg is consistently stronger than Magnussen, while Bearman’s debut races show potential but mixed results.
- **Visa Cash App RB:** Tsunoda outperforms Ricciardo initially, while Lawson shows improvement after replacing Ricciardo mid-season.
- **Williams:** Albon is consistently ahead of Sargeant, with Colapinto narrowing the gap after replacing Sargeant.
- **Alpine:** Gasly outperforms Ocon consistently, with Doohan’s debut at Abu Dhabi showing a learning curve.

### Track-Specific Strengths
- **Circuit-Specific Performance:** Drivers like Verstappen excel on high-speed tracks (e.g., Monza, Silverstone), while Norris and Piastri show strength on street circuits (e.g., Monaco, Singapore).
- **Team Advantages:** Teams like Red Bull and McLaren demonstrate track-specific strengths, with Red Bull dominating in Austria and McLaren excelling in Miami and Hungary.

## Contribution
This project is open for contributions. If you’d like to add new analyses, improve visualizations, or fix bugs, please fork the repository, make your changes, and submit a pull request.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details (if applicable, create a `LICENSE` file with the MIT License text).

## Acknowledgments
- Thanks to the `fastf1` team for providing the tools to access and analyze Formula 1 data.
- Appreciation to the F1 community for insights and data sources that inspired this analysis.
