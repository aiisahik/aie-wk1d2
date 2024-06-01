# Prompt Engineering Experiment

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

 
