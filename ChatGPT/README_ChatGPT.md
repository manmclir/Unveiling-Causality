Here is an explanation for file in this folder:

ChatGPT_experiment.ipynb:
This is a notebook that was used as a scratch pad to experiment with different ChatGPT prompts.

Combine_O_EDA_ChatGPT.ipynb:
This notebook contains the methods that combine the original, EDA augmented, and ChatGPT generated dataset.

Create_ChatGPT_Dataset.ipynb:
This notebook contains the functions that were used to prompt ChatGPT and generate the raw ChatGPT dataset.

Process_ChatGPT.ipynb:
This notebook processes the raw ChatGPT generated dataset into datasets that can be used by the BoschAI model to train. 

filter_dataframe_l: This takes in a df and a word list and removes every entry that does not have a word in the word list in the text column.

process_text: This function confirms that there are no words outside of the bounds of the bracket wrapping and it capitalizes all of the tags.

remove_wrapping: This function removes the bracket wrapping that usually surrounds the causal_w_text column
