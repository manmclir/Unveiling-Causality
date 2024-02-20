Here is an explanation for file in this folder:

ChatGPT_experiment.ipynb:
This is a notebook that was used as a scratch pad to experiment with different ChatGPT prompts.

There are two different functions that creates datasets: create_dataset and create_dataset_s 
create_dataset inputs in 4 sentences for every prompt to ChatGPT and create_dataset_s only inputs in one sentence to the prompt. 

Combine_O_EDA_ChatGPT.ipynb:
This notebook combines the EDA, ChatGPT, and original training dataset into one dataset that ready to be trained on BoschAI.

Create_ChatGPT_Dataset.ipynb:
This notebook contains the functions that were used to prompt ChatGPT and generate the raw ChatGPT dataset.

conv_s2: This function creates the part of the prompt which gives an example based on an entry of the original training dataset. The format is such: s = "Here is an example of the tags used in the appropriate scheme:\n" + sentence + "\nWhere the cause in the scheme is: " + cause + "\nThe effect in the scheme is: " + effect + "\nThe signal in the scheme is: " + signal + "\n"
cause effect and signal are the parts of the sentence that are enclosed between those tags.


create_sample_f2: This function puts together the full prompt and uses query_Chat to query ChatGPT using the prompt that it puts together. 

append_to_csv_file: This function appends a df entry to a csv file. This was used so that the csv file was updated as more ChatGPT queries were answered.

query_Chat: This takes a prompt and prompts ChatGPT with the prompt given. The function returns the response from ChatGPT as a string.



Process_ChatGPT.ipynb:
This notebook processes the raw ChatGPT generated dataset into datasets that can be used by the BoschAI model to train. 

filter_dataframe_l: This takes in a df and a word list and removes every entry that does not have a word in the word list in the text column.

process_text: This function confirms that there are no words outside of the bounds of the bracket wrapping and it capitalizes all of the tags.

remove_wrapping: This function removes the bracket wrapping that usually surrounds the causal_w_text column

In Process_ChatGPT.ipynb there are two big code blocks that are mainly responsible for producing CNC_chatgpt+orig_output_no_space6.csv and CNC_chatgpt+orig_output_no_sig65.csv. The code block does the normal process for turning a dataset that only has causal_w_text into a full dataset that has all the columns that the CNC training data has. Aside from converting the dataset it also applies several changes to the dataset which ensure that the tags in the sentences are applied correctly. In the BoschAI model there are sequences of tags that are not possible and if the dataset is left unchanged the model will accidentally identify certain entries as having an illegal sequence of tags. The changes are to prevent that for cases where it is accidental and for cases where it is not it deletes the entry.
