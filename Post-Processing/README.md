# This folder deals with fixing data issues in augmented sentences.

- Converting arg and sig in causal_text_w_pairs into uppercase.
- Deleting words in causal_text_w_pairs appearing outside of square brackets.
  ## Example:
  atomic number ['<ARG1>opp atomic number atomic number stages dharna in atomic number karna assembly</ARG1> <SIG0>over</SIG0> <ARG0>finance bill</ARG0>']
  ## Output:
  ['<ARG1>opp atomic number atomic number stages dharna in atomic number karna assembly</ARG1> <SIG0>over</SIG0> <ARG0>finance bill</ARG0>']

  Then create a text column by removing arg, sig and brackets again
  
- Remove all square brackets in the causal_text_w_pairs and add at the [ start and ] end

  ## Example:
- ['the memorandum given to chief minister harish rawat , on saturday , read <ARG0>the stone crushers working in the area</ARG0> <SIG0>will [ be the cause of</SIG0> <ARG1>dust and health problems</ARG1> which will ] [ and the dust from the stone crushers would destroy agriculture ] [ be the cause of <ARG0>dust and health problems</ARG0> which <SIG0>will ] [ and the dust from the stone crushers would destroy agriculture ] [ be the cause of dust and health problems which will ] [ and <ARG0>the dust from the stone crushers</ARG0> <ARG1><SIG0>would destroy</SIG0> agriculture</ARG1> ] ']
- ['on th , subgenus chen daoxiang , the headspring of the taiwanese united states army fort in hong kong , enunciate <ARG1>the military machine was ascertain to protect  [ the ]  ']


  ## Output:
- ['the memoranda break to headman parson harish rawat , on sat , interpret <ARG0>the i f stone crusher solve in the area</ARG0> <SIG0>will  be the get of</SIG0> <ARG1>dust and wellness problems</ARG1> which will   and the junk from the i f stone crusher would ruin department of agriculture   be the get of <ARG0>dust and wellness problems</ARG0> which <SIG0>will   and the junk from the i f stone crusher would ruin department of agriculture   be the get of junk and wellness trouble which will   and <ARG0>the junk from the i f stone crushers</ARG0> <ARG1><SIG0>would destroy</SIG0> agriculture</ARG1>  ']
- ['on th , subgenus chen daoxiang , the headspring of the taiwanese united states army fort in hong kong , enunciate <ARG1>the military machine was ascertain to protect  the  ']

## num_rs
- The file has only num_rs=1
