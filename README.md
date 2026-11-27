# Spaceship Titanic

This is my work in progress for Kaggle's [Spaceship Titanic competition](https://www.kaggle.com/competitions/spaceship-titanic). The goal is to predict which passengers were transported to another dimension.

## Open the notebook

1. Open [spaceship_titanic.ipynb](spaceship_titanic.ipynb) in VS Code with the Python and Jupyter extensions.
2. Select a Python kernel with `pandas` installed and run the cells from top to bottom.

## Preprocessing

1. Fill one or two missing charges with zero when all recorded charges for that passenger are zero. The five spending fields are RoomService, FoodCourt, ShoppingMall, Spa, and VRDeck.
2. Add the five charges to calculate `Total_Spend`.
3. Fill missing `CryoSleep` values with `False` when any recorded charge is positive and with `True` when `Total_Spend` is zero. Keep the original `CryoSleep` values.

The notebook prints the remaining missing `CryoSleep` count and writes `null_inspection.csv` for inspection.

## Data

The repository includes `train.csv`, `test.csv`, and `sample_submission.csv` from the [Kaggle Spaceship Titanic competition dataset](https://www.kaggle.com/competitions/spaceship-titanic/data), licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).

## What I'm exploring

The notebook loads the training data and outlines questions about whether transport rates vary by CryoSleep status, age, home planet, destination, or onboard spending. I also plan to look at whether passengers who shared a cabin, surname, or travel group were transported together.
