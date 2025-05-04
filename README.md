# Badminton-PageRank
Project Title: Dynamic PageRank for Badminton: A Data-Driven Ranking System and Its Applications  
Candidate Number: LHLW8

This repository compiles the Appendix, including all relevant codes and datasets for the project. It contains three main folders as described below:
| Folder Name  | Description                                                                                  |
|--------------|----------------------------------------------------------------------------------------------|
| Models       | Contains the main RMarkdown files to run the PageRank, Bradley-Terry, and Elo models, including files used to test predictive accuracy. |
| Plots        | Contains the code and datasets used to generate all plots in the thesis.                      |
| Application  | Contains the RMarkdown and Excel files used to run the simulations for the two applications.  |

In the main folder, the following files are included:

| File Name                     | Description                                                                                         |
|-------------------------------|-----------------------------------------------------------------------------------------------------|
| Web_Scraper.ipynb             | Code used to webscrape datasets from [https://badmintonranks.com](https://badmintonranks.com).     |
| PlayerID_List.xlsx            | Mapping of PlayerID and player names by discipline.                                                  |
| TournamentID_List.xlsx        | Full list of information on the 670 tournaments investigated.                                        |
| WR 2025-01-14 (Week-03).pdf   | Full BWF official ranking during Week 5, 2024 (used in the tournament entry simulator application, Section 5.1). |

---

Folder: Models

| File Name                      | Description                                                                                          |
|--------------------------------|------------------------------------------------------------------------------------------------------|
| RAW.csv                        | Full compilation of extracted dataset.                                                               |
| Split.rmd                      | Used to split the RAW dataset by discipline, match frequency, and train-test split.                  |
| PR.rmd                         | Functions to generate rankings using the PageRank algorithm (PR1–PR5).                              |
| Reference_Models.rmd           | Functions to generate rankings using the Elo rating system and Bradley-Terry model.                 |
| Brier_Score.rmd                | Code to calculate Brier score for the models.                                                       |
| Predictive_Analysis.rmd        | Code to calculate predictive accuracy using Methods 1, 2, and 3.                                    |
| Minimum_Match_Frequency.xlsx   | Calculation of the “Information Score” to determine minimum match frequency by discipline.          |
| Brier_Scores.xlsx              | Compilation of Brier scores for all models.                                                         |
| Predictive_Accuracy.xlsx       | Compilation of predictive accuracy results for all models (by method).                              |
| Ranking_Results_Compiled.xlsx  | Compilation of PlayerID, rank, and PR/Elo/BT scores for all disciplines                                                |
| Correlation_Matrix.xlsx        | Correlation matrix for all models.                                                                  |
| tourID.csv                     | List of tournaments given time-boost (PR5).                                                         |
|Discipline-specific files (using abbreviations):
MS = Men’s Singles, WS = Women’s Singles, MD = Men’s Doubles, WD = Women’s Doubles, XD = Mixed Doubles.|
| TOP_MS.csv                     | Dataset of players with more than the minimum match frequency for Men’s Singles.                    |
| TOP_MS_TRAIN.csv               | 80% training dataset from TOP_MS.                                                                  |
| TOP_MS_TEST.csv                | 20% test dataset from TOP_MS.                                                                      |
| ELO_MS.csv, BT_MS.csv          | Final reference model results for Men’s Singles.                                                   |
| PR1_MS.csv to PR5_MS.csv       | Final PageRank variant results for Men’s Singles.                                                  |

---

Folder: Application

| File Name                       | Description                                                                                             |
|---------------------------------|---------------------------------------------------------------------------------------------------------|
| Tournament_Simulator.rmd        | Code to run the simulation for the Tournament Entry Simulator application.                              |
| Betting.rmd                     | Code to run the simulation for creating the betting odds table.                                         |
| Tournament_Simulator.xlsx       | Results of the Tournament Entry Simulator on reference players (refer to Section 5.1).                  |
| Betting_Odds.xlsx               | Results of betting simulation on Women’s Singles at All England 2025 (refer to Section 5.2).            |
| APPLICATION_MS.csv, APPLICATION_WS.csv | Edited Men’s and Women’s Singles datasets used in the applications.                                          |
| APP_PR5_WS.csv, APP_BT_WS.csv, APP_ELO_WS.csv | New PR5, BT, and Elo model runs on edited Women’s Singles dataset.                                      |
| Tournament_AllEngland_PR5.csv   | Full entry list of players and PR5 scores for All England 2024 tournament.                               |
| Tournament_OrleansMasters_PR5.csv | Full entry list of players and PR5 scores for Orleans Masters 2024 tournament.                           |
| Bet_BT.csv, Bet_PR5.csv, Bet_ELO.csv, Bet_H2H.csv | Lists of players with BT strength, PR5 scores, Elo ratings, and Head-to-Head wins for the betting application. |

---

Folder: Plots

| File Name                  | Description                                                        |
|----------------------------|--------------------------------------------------------------------|
| Plots.rmd                 | Code to generate figures used in the thesis report.                 |
| Line-MS.csv, Heatmap-MS.csv, Scatter-MS.csv | Datasets used in Plots.rmd for Men’s Singles plots.                               |
| Brier_Scores_v2.csv        | Updated Brier score dataset used for plotting.                      |
| Predictive_Accuracy_v2.csv | Updated predictive accuracy dataset used for plotting.              |
| Information_Score.csv      | Dataset used to calculate and plot Information Score.              |
