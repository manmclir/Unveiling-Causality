This folder contains the python code to transform our augmented data into the CSV file format with the following columns:

Columns:

1. corpus [str] : corpus name
2. doc_id [str] : document name
3. sent_id [int] : sentence id
4. eg_id [int] : each sentence can have multiple relations/examples, this indicates the example id count
5. index [str] : example unique id
6. text [str] : example input text
7. causal_text_w_pairs [list] : list of up to three causal target marked text that includes (<ARG0>,<ARG1>,<SIGX>) annotations. if no causal relation exists, an empty list is returned.
8. num_rs [int] : length of list in causal_text_w_pairs
