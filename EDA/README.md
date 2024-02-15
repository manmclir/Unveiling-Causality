Download the code from:
https://github.com/jasonwei20/eda_nlp/tree/master

alpha_sr=0.1, alpha_ri=0.1, alpha_rs=0.0, p_rd=0.0, num_aug=5 are the values set in eda function


eda_2_output_cleaned_train_subtask2.txt is generated using the eda code provided.

Also, to separate the sentences similar to each other if num_rs>1, the text cleaning function is modified and can be viewed in text_clean.ipynb file


The code as been executed using the following command:

python code/augment.py --input=data/output_cleaned_train_subtask2.txt --output=data/eda_2_output_cleaned_train_subtask2.txt --num_aug=5 --alpha_sr=0.1 --alpha_rd=0.0 --alpha_ri=0.1 --alpha_rs=0.0
