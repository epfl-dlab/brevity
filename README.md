# Causal Effects of Brevity on Style and Success in Social Media

This repository provides information about the data collected and used in our CSCW 2019 paper.

### The description of the dataset

For each of the original input tweets, the dataset contains a dictionary with the following information:

```
-original_tweet_text: The text of the original input tweets

-Q1: The first comprehension question
-Q1_possible_anser1: The first possible answer to the first question
-Q1_possible_anser2: The second possible answer to the first question
-Q1_possible_correct_answer: The correct answer to the first question

-Q2: The second comprehension question
-Q2_possible_anser1: The first possible answer to the second question
-Q2_possible_anser2: The second possible answer to the second question
-Q2_possible_correct_answer: The correct answer to the second question

-Q3: The third comprehension question
-Q3_possible_anser1: The first possible answer to the third question
-Q3_possible_anser2: The second possible answer to the third question
-Q3_possible_correct_answer: The correct answer to the third question

-treated_versions: a dictionary with information about each treated version
      -10-20%: Information about the 10-20% level of relative shortening
        -tweet: The text of the edited tweet
        -success_prob: Probability that the edited version is more successful 
                       compared to the original tweet, measured as the fraction
                       of the votes in favor of the edited version. This is probability
                       of success as defined in the subsection "Measuring the effect of
                       brevity on message success"
      ...

      -80-90%: Information about the 80-90% level of relative shortening
        -tweet
        -success_prob

      -baseline: Information about the baseline
        -tweet
        -success_prob
```

It is necessary to specify the encoding in order to load the file successfully. For example, to inspect the example from the
publication in the Table 3:

```python
import json
import pprint

with open('brevity_dataset.json', encoding="utf-8") as file:
    data = json.load(file)
  
pprint.pprint(data["4"])
```

### Reference

Please cite the paper when using the data:

**Causal Effects of Brevity on Style and Success in Social Media,** Kristina Gligori&#263;, Ashton Anderson and Robert West. *ACM Conference on Computer-Supported Cooperative Work and Social Computing (CSCW), Austin, Texas, November 2019.* 
[https://dlab.epfl.ch/people/west/pub/Gligoric-Anderson-West_CSCW-19.pdf](https://dlab.epfl.ch/people/west/pub/Gligoric-Anderson-West_CSCW-19.pdf)
