# SC1015_MiniProject
# Predicting the performance of soccer players

SC1015 FCE3 Group 9 --- Lennard Ng Weijie, Raja Muthu

Dataset: https://www.kaggle.com/datasets/vivovinco/20212022-football-player-stats

Problem statement: Football managers have a tough time deciding which players to buy, release, or play annually.

## 1. Cleaning our dataset
### Dataset
Our dataset contains the average performance statistics of football players from the years 2021 to 2022. It contains 143 different variables, and a total of 2921 players.

## Cleaning
a. There are 4 different main roles in football. Forward, Midfielder, Defender, and Goalkeeper. The dataset includes players of hybrid positions (e.g. Forward/Midfielder) and we decided to drop these hybrid players to give us a more accurate representation of the role itself.
b. Not all the variables were useful in predicting the stats for each role. As such, we singled out different target variables, as well as predictors for each role. The list is as follows:
#### Forwards:
Target: Goals per Shot (G/Sh) and Goals per Shot on Target (G/SoT)

Predictors: Goals, Shots, Shots on Target (SoT), Shot-Creating Actions (SCA), Goal-Creating Actions (GCA), Touches in Attacking Penalty Area (TouAttPen) and Carries into 18-yard box (CPA).
#### Midfielders:
Target: Percentage of complete passes at short, medium and long ranges (PasShoCmp%, PasMedCmp%, PasLonCmp%)

Predictors: Number of complete passes at short, medium and long ranges (PasShoCmp, PasMedCmp, PasLonCmp), Progressive Passes (PasProg), Completed Passes into the 18-yard box (PPA), Interceptions (Int), Tackles (Tkl), Carries (Carries), Progressive Carries (CarProg), Shot-Creating Actions (SCA) and Goal-Creating Actions (GCA)
#### Defenders:
Target: Tackles (Tkl), Clearances (Clr), Interceptions (Int)

Predictors: Blocks of shots and passes (BlkSh, BlkPass), TklDef3rd, TklMid3rd (Tackles in defensive and midfield areas), Passing accuracy, especially for long balls (PasTotCmp%, PasLonCmp%), Aerial duels won (AerWon%, AerWon)

## 2. Exploration

## 3. Machine learning
We used 3 machine learning models: Linear regression, Random forest, and Gradient boosting.

As seen in our correlation matrix during our exploration, many of the variables are not linearly correlated with each other. hence we sought out different predictive modelling techniques to deal with non-linear relationships.

## 4. Conclusion
### Result analysis
Linear regression largely only worked for Forwards.

Random forest was effective in predicting the stats of Forwards and Midfielders.

Gradient boosting was effective in predicting the stats of Forwards and Defenders.

### Data-driven insights
Teams can predict the relevant stats of players depending on their roles using the respective models. They are able to get a more accurate representation of their skills, such as Goals per Shot showing how accurate the player is.

This aids team managers in their decision-making processes regarding the players.

## Individual contributions
Finding the dataset and problem statement: Muthu
Cleaning and EDA: Lennard & Muthu
Machine learning models: Lennard
Conclusion: Lennard & Muthu
Notebook: Muthu

## References
- https://www.kaggle.com/datasets/vivovinco/20212022-football-player-stats
- https://www.ibm.com/topics/random-forest
- https://www.datacamp.com/tutorial/guide-to-the-gradient-boosting-algorithm
