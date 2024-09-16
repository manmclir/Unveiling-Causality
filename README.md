# EASY DATA AUGMENTATION

## Data_Cleaning
- Run the code eda_data_cleaning.ipynb
- Cleans the data and stores into cleaned_output_train_subtask2.csv
- Write the cleaned text and num_rs columns to the text file output_cleaned_train_subtask2.txt

## EDA
- Update the text cleaning function **get_only_chars(line)** as specified in text_clean.ipynb
- Run the code using the updated parameters num_aug=5 --alpha_sr=0.1 --alpha_rd=0.0 --alpha_ri=0.1 --alpha_rs=0.0
- eda_2_output_cleaned_train_subtask2.txt is generated as the result of the eda augmentation

## ChatGPT
- Contains the notebook files that generate the ChatGPT dataset, the notebook files to process the data to create the final training dataset, and the datasets used in the BoschAI model training

 ## Data_Transformation
 - Run the code Data_Transformation.ipynb
 - Output file generated eda_2_output_transformed_train_subtask2.csv

## Overview Of Easy Data Augmentation

### Data Cleaning-1
- Input File: train_subtask2_grouped.csv
- Code: eda_data_cleaning.ipynb (Function remove_backslash())
- Output File: cleaned_output_train_subtask2.csv

## Data Cleaning-2
- Input File: cleaned_output_train_subtask2.csv
- Code: eda_data_cleaning.ipynb
- Output File: output_cleaned_train_subtask2.txt

## EDA
- Input File: output_cleaned_train_subtask2.txt
- Code repository: https://github.com/jasonwei20/eda_nlp/tree/master
- Modifications proposed in: text_clean
- Code execution: python code/augment.py --input=data/output_cleaned_train_subtask2.txt --output=data/eda_2_output_cleaned_train_subtask2.txt --num_aug=5 --alpha_sr=0.1 --alpha_rd=0.0 --alpha_ri=0.1 --alpha_rs=0.0
- Output File: eda_2_output_cleaned_train_subtask2.txt
  
## Data Transformation
- Input File: eda_2_output_cleaned_train_subtask2.txt
- Code: Data_Transformation.ipynb
- Output File: eda_2_output_transformed_train_subtask2.csv

# Data Post-Processing
- Input File: eda_2_output_transformed_train_subtask2.csv
- Code: Post-Processing-test.ipynb
- Output: del_4_processed_eda_2_output_transformed_train_subtask2.csv
