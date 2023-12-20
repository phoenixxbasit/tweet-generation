# Tweet Generator using Markov Chain

This repository contains a Jupyter Notebook script for generating tweets using a Markov Chain model. The script utilizes a dataset of tweets, extracts relevant information, and trains a Markov model to generate new, realistic-sounding tweets. Below is an organized overview of the project.

## Table of Contents

- [How to Run](#how-to-run)
- [Importing The Data](#importing-the-data)
- [Extracting and Filtering Tweets](#extracting-and-filtering-tweets)
- [Cleaning Text](#cleaning-text)
- [Training the Markov Model](#training-the-markov-model)
- [Importing the Trained Model](#importing-the-trained-model)
- [Saving the Trained Model](#saving-the-trained-model)
- [Generating Tweets](#generating-tweets)

## How to Run

To run the Jupyter Notebook, follow these steps:

1. Clone the repository to your local machine.
2. Install Jupyter Notebook if you haven't already:

   ```
   pip install jupyter
   ```

3. Navigate to the project directory in the terminal.
4. Launch Jupyter Notebook:

   ```
   jupyter notebook
   ```

5. Open the notebook file (`code.ipynb`) in the Jupyter Notebook interface.
6. Execute the cells in sequence using Shift + Enter.

## Importing The Data

The script begins by importing necessary libraries and loading tweet data from multiple CSV files in the 'Data' directory. It combines these datasets, extracting relevant information such as text and retweet count.

## Extracting and Filtering Tweets

1. **Extracting Only English Tweets:** Filters the dataset to include only English tweets.
2. **Extracting Only Text and Retweet Count Column:** Selects only the 'text' and 'retweetcount' columns from the filtered dataset.
3. **Getting Only Tweets with More Than 1000 Retweets:** Further filters tweets to include only those with more than 1000 retweets.

## Cleaning Text

The script defines a function to clean the text of tweets by removing links, URLs, hashtags, non-ASCII letters, and punctuations. The cleaned text is then tokenized and processed for further analysis.

## Training the Markov Model

1. **Markov Model Generation Function:** Defines a function to create a Markov model based on the cleaned text. The model calculates transition probabilities between states.
2. **Training Our Model:** Applies the Markov model function to the cleaned tweet data, generating a trained model.

## Importing the Trained Model

Demonstrates how to load the trained Markov model from a saved JSON file.

## Saving the Trained Model

Saves the trained Markov model to a JSON file for future use.

## Generating Tweets

Defines a function to generate tweets using the trained Markov model. Demonstrates the generation of 20 tweets starting with the seed phrase "usa is".

> [!Important]
>
> Feel free to explore and modify the script for your specific use case. If you have any questions or suggestions, please open an issue or contribute to the project. Happy tweeting!
