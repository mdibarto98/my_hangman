# my_hangman
Hangman ML model:

I have implemented a Deep Learning Model which at each step of the hangman game takes as inputs:

- The obscured encoded status of the word we have been trying to guess since the beginning of the hangman simulation
- The encoded letters the model has guessed so far since the beginning of the hangman simulation
- The (1-5) n-grams probabilities
  
The model returns the probability associated with all 26 letters in the English dictionary and guesses the letter with the highest probability among the letters we have not guessed yet.
During training the target variable is the frequency of each letter in the target word, normalized to sum to 1.
The model is trained for a few epochs using Categorical Cross-Entropy as loss function.
