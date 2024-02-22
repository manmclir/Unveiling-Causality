Here is an explanation for the datasets utilizied

train_subtask2_grouped.csv: This is the original training data set from which all augmentations are based on.


EDA+CNC_chatgpt+orig2.csv: This is the final dataset that combines the ChatGPT generated dataset with the EDA augmented dataset and the Original training dataset. This dataset also has the original training dataset in the beginning.


CNC_synth_copy2.csv: This is the raw unprocessed ChatGPT generated responses that was processed to create CNC_chatgpt+orig_output_no_sig65.csv and CNC_chatgpt+orig_output_no_space6.csv. 


CNC_eda_o+orig_output55.csv: This is the EDA dataset that was used in training and incorporated in EDA+CNC_chatgpt+orig2.csv. This dataset also has the original training dataset in the beginning.


CNC_chatgpt+orig_output_no_space6.csv: This is the ChatGPT generated dataset entries that have all of the tags. It is incorporated in EDA+CNC_chatgpt+orig2.csv. This dataset also has the original training dataset in the beginning.


CNC_chatgpt+orig_output_no_sig65.csv: This is the ChatGPT generated dataset entries that do not have the signal tags. It is incorporated in EDA+CNC_chatgpt+orig2.csv. This dataset also has the original training dataset in the beginning.


eda_2_output_transformed_train_subtask2.csv: This is the EDA augmented dataset that was later processed using the Process_EDA.ipynb into CNC_eda_o+orig_output55.csv which was used to get results. 
