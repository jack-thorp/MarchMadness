# March Madness Predictor
- ***Last Updated***: 04/01/2025
- ***Author*** : Jack Thorp

### Background:
Back in college, I often used [Kaggle](https://Kaggle.com) to find datasets for my statistic and econometric classes. As an avid basketball fan (go Clemson and Tar Heels!), Kaggle's March Madness contest always intrigued me. I didn't manage to enter the 2025 competition, but I did want to play around to see how close I could get using the contest's datasets!

### Overview:
This repository provides a Jupyter notebook that leverages historical regular-season data, NCAA tournament seeding, and KenPoms rankings to forecast the probability of one NCAA team beating another. A Random Forest classifier is used to make these predictions. In the first quick attempt (trained on years '15-'22), the model achieved **72.4% accuracy** on the validation set (years '23 & '24).


### Features:
- **Automated Data Pipeline**: Builds team-level statistics and merges external rankings (KenPom).
- **Rolling Stats**: Uses recent performances to capture hot/cold streaks leading into tournament.
- **Tournament Matchup Simulation**: Predicts head-to-head outcomes for any seeded team in the 2025 bracket.

### Getting Started:
1. Clone this repo and open `MarchMadnessPredictor.ipynb`
2. Install requirements
3. [Download Datafiles](https://www.kaggle.com/competitions/march-machine-learning-mania-2025) from Kaggle competition
4. Run each cell in the notebook to:
    - Load and preprocess the data
    - Train the Random Forest classification model
    - Generate predictions for upcoming or hypotetical matchups

### Repo Structure:
```
MarchMadnessPredictor/
├── readme.md
├── MarchMadnessPredictor.ipynb   # main notebook for capturing predictions
├── data/                         # contains raw data (stored in personal AWS and not repo)
├── output/                       # contains model predictions (stored in personal AWS and not repo)
└── archive/                      # previous predictor versions
```

### Notes & Future Plans:
- Tweak hyperparams (i.e., rolling window size, number of estimators, what external ranking metric)
- Investigate which features have the strongest predictive power
- Research other successful IVs
- Continue exploring other models as we further refine input
- build accuracy graph to visualize in next readme.md file
