
Sampling is a technique employed to gain insights into a population by analyzing statistics from a representative subset, eliminating the need to examine every individual. In addressing an initial dataset imbalance, where there were 763 non-fraudulent cases and only 9 fraudulent cases, an oversampling approach was implemented. This involved generating additional instances of the minority class (fraudulent cases) to match the majority class (non-fraudulent cases), resulting in a balanced dataset consolidated into a single data frame.

Various sampling techniques were employed:

Simple Random Sampling: This involves randomly selecting samples from the population without any specific order.

Systematic Sampling: In this method, samples are selected at regular intervals after a random start, providing a systematic representation of the population.

Cluster Sampling: This technique entails randomly selecting clusters from the population and including all members within those clusters in the sample.

Stratified Sampling: The population is divided into subgroups based on specific criteria, and samples are then taken from each subgroup, ensuring representation from all segments.

Bootstrap Sampling: Resampling with replacement is performed to create multiple samples from the original dataset. This helps in assessing the variability of statistical estimates.

Following the generation of five distinct samples using these techniques, five models were applied to each sample. The accuracies of each model for a given sample are summarized in the following table:

| Sample Technique      | Random Forest | Logistic Regression | Naive Bayes      | Decision Trees   | KNN              |
|-----------------------|---------------|---------------------|------------------|------------------|------------------|
| Simple Random Sampling| 0.9870        | 0.8831              | 0.7013           | 0.9610           | 0.8701           |
| Systematic Sampling   | 1.0000        | 0.8926              | 0.7450           | 1.0000           | 0.9329           |
| Cluster Sampling      | 1.0000        | 0.9670              | 1.0000           | 1.0000           | 0.9890           |
| Stratified Sampling   | 1.0000        | 0.9030              | 0.7239           | 0.9925           | 0.9552           |
| Bootstrap Sampling    | 1.0000        | 0.9250              | 0.7500           | 0.9625           | 0.9375           |

In above table, each row corresponds to a sampling technique, and each column represent the accuracy achieved by each model applied to the respective sample generated using that respective technique.
<br>
### The RANDOM FOREST outperformed all other models when applied to Stratified Sampling Technique.
