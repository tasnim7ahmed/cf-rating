# Codeforces Rating Predictor

## Overview
This project aims to predict the rating changes of participants in Codeforces contests using a reinforcement learning approach. The model takes into account various features including old ratings, contest start times, durations, and problem categories (tags) to make predictions.

## Dataset
The dataset is derived from the Codeforces API, containing historical contest data for each participant. Each record in the dataset includes:
- Old Rating
- New Rating
- Contest Duration
- Contest Start Time
- Problem Tags

## Model Architecture
The model uses a Q-Learning based neural network, comprising of:
- Input Layer: Size corresponds to the number of features (old rating, start time, duration, and problem tags).
- Hidden Layer: A fully connected layer with 64 neurons.
- Output Layer: Produces a rating prediction.

## Data Processing
Data processing involves fetching data from the Codeforces API, transforming problem tags into binary features, and normalizing time and duration data.

## Running the Notebook
To run the notebook:
1. Ensure you have Python 3.x installed.
2. Install necessary libraries: `torch`, `numpy`, `pandas`, and `requests`.
3. Run the Jupyter notebook: `predictor.ipynb`.

## Evaluation
The model's performance is evaluated using Root Mean Squared Error (RMSE) between the predicted and actual rating changes.

## Limitations
- The model's accuracy is highly dependent on the quality and quantity of the data.
- API rate limits may restrict real-time data fetching.

## Future Work
- Incorporate more features like user's problem-solving history.
- Explore other reinforcement learning algorithms like Proximal Policy Optimization (PPO).

## License
This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.
