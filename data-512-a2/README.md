# Data 512 Assignment 2: Bias in data

## Selected and downloaded datasets are:
1- Aggression dataset available at: https://figshare.com/articles/dataset/Wikipedia_Talk_Labels_Aggression/4267550 <br>
2- Toxicity dataset avaialble at: https://figshare.com/articles/dataset/Wikipedia_Talk_Labels_Toxicity/4563973

## Motivation of this project:
To investigate the gender inequality in crowdworkers that annotated  Wikipedia Talk corpus of thousands online discussion posts in two Aggression and Toxicity datasets (i.e. skewed labeller gender distribution). Furthur looked into how each gender inclinded to label the comments as "aggressive" or "toxic" (exploring the difference in labeling behavior). I wanted to look and see how the difference in gender distribution and difference in labeling behavior could affect the models that are based on these annotations.

## Questions investigated:

- Aggression dataset
Q1- a) Is there a difference in the number of men and women among the crowdworkers, and how is it different from the general population? b) Which gender annotates comments as more aggressive in the aggression datasets?


- Toxicity dataset
Q2- a) Is there a difference in the number of men and women among the crowdworkers who annotated the Wikipedia Talk corpus for Toxicity and how is it different from the general population? b) Which gender annotated comments as more toxic in the toxicity datasets?

## Results:
- Gender distribution:<br>
The distribution of men and women in both datasets (Aggression and Toxicity) are biased. In both datasets number of men outweight the number of women. In the aggression dataset I found that there are more men annotators than women (1349 vs. 840). In other words, only about 38% are women. Again, in the "Toxicity" dataset, the crowdworkers consist of more male annotators (2327 vs. 1263). In other words only about 35% are women.<br>

|.    | Men (n) | Women (n)|% Women
| --- | --- | --- |---|
| Aggression dataset  | 1349 | 840 | 38%|
| Toxicity dataset  | 2327 | 1263 | 35%

Labeling behavior by gender:
<br>
- Exploratory analysis shows that there is a difference in how women label comments compared to men. Based on  Graph 1, we can see that women are more prone to annotate the words as aggressive. About 20% of women and 18% of men tend to annotate a comment as aggressive. Based on Graph 2, we can see that about 16% of women and 14% of men tend to annotate a comment as toxic.
<br>

![Graph 1](/data-512-a2/graph_1.png)

<br>

![Graph 2](/data-512-a2/graph_2.png)
<br>
Comparing the results in two datasets:
- Gender distribution difference exists in both datasets (more men than women among crowdworkers. 
- Labeling behavior for aggression and toxicity is different when comparing men and women. 
