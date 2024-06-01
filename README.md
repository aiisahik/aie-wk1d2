# Prompt Engineering Experiment

## Setup

for the system / prompt template, we either used the basic version or the engineered version. 

#### Basic Version 
system_template = """\
You are a helpful assistant.
"""
user_template = """
{input}
"""

#### Engineered Version 
system_template = """\
You are a helpful assistant specializing in tricky mental and logical problems.
"""
user_template = """
You MUST do the following!
{input} 
Provide a clear response that is faithful to the original query.
Make sure your answer has been verified for correctness.
Do not assume any facts without careful analysis.
Think through things step by step before giving the final answer.
You will be penalized if you fail to do all of the above.
I'm going to tip $100 for a better solution!
"""

We tested both of the templates on 5 different questions: 
1. """Billy wants to get home from San Fran. before 7PM EDT. It's currently 1PM local time. Billy can either fly (3hrs), and then take a bus (2hrs), or Billy can take the teleporter (0hrs) and then a bus (1hrs). Does it matter which travel option Billy selects?"""
2. """Evaluate the financial costs of climate change impacting southern Spain over the next 20 years"""
3. """Three boys agree to divide a bag of marbles in the following manner. The first boy takes one more than half the marbles. The second takes a third of the number remaining. The third boy finds that he is left with twice as many marbles as the second boy."""
4. """# There are 2 people living next to each other. Both have a pet. One of them has a dog and the other a cat. The Englishman lives in the red house and the Frenchman lives in the blue house. The owner of the blue house has a cat. Who has the dog?"""
5. """A car travelling at a speed of 20 kph left a certain place at 3:00 p.m. At 5:00 p.m. another car departed from the same place at 40 kph and travelled the same route. In how many hours will the second car overtake the first?"""

Finally, we tested all questions and prompt tempaltes on both the "gpt-3.5-turbo" and "gpt-4o" models. 


## Results: 

| Attempt | GPT3.5 Basic | GPT3.5 Engineered   | GPT4o Basic    | GPT4o Engineer    |
| :---:   | :---: | :---: |:---: |:---: |
| Billy wants to get home | 7/5/4   | 7/9/8 👍   |9/10/8   |9/10/10   |
| climate change | 8/9/7   | 7/6/8   |9/10/9   |8/6/7 👎  |
| bag of marbles | 8/9/7   | 7/9/3 👎   |8/9/10*   |4/7/6 👎  |
| Englishman and Frenchman | 8/10/10   | 8/8/10   |10/10/10   |10/10/10   |
| car travelling  | 10/10/10   | 9/10/10   |9/10/10   |9/10/10   |




## Thoughts

1. the "Billy wants to get home" problem is the only question where prompt engineering made a significant difference to the accuracy of the output. For most of the other questions, the prompt engineering didn't make too much of a difference 
2. In the case of the bag of marbles (the hardest question), the prompt engineering techiques actually made things WORSE for both GPT3.5 and GPT4o 
3. GPT4o was not able to get ANY improvements from the prompt engineering - if anything the engineering hurt results for 2 of the questions. This suggests that OpenAI probably thought of it as kinda undesirable to have folks offer tips or use weird tactics to get a better resupose from gpt - therefore in the later models, they probably made sure these strategies no longer yields any benefit 
4. The paper was submitted on 26 Dec 2023, and was last revised 18 Jan 2024. Probably lots of changes since then. AI space is moving too quickly. 

 
