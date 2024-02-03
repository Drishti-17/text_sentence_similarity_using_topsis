# Sentence Similarity Using Topsis

# TOPSIS:-

![TOPSIS-method-algorithm](https://github.com/Drishti-17/sentence_similarity_using_topsis/assets/91721425/86dc1c04-dd07-4f70-98c9-fc5b7d11cbce)


TOPSIS, which stands for Technique for Order of Preference by Similarity to Ideal Solution, is a multi-criteria decision analysis method used in decision-making processes. It is a mathematical approach that helps in selecting the best alternative from a set of alternatives based on their similarity to an ideal solution.

Here's a brief overview of how TOPSIS works:

1. **Identify Criteria:** Determine the criteria that will be used to evaluate the alternatives. These criteria should be relevant to the decision at hand and measurable.

2. **Normalize the Decision Matrix:** Create a decision matrix where each row represents an alternative, and each column represents a criterion. Normalize the matrix to bring all criteria to a common scale, which is usually between 0 and 1.

3. **Determine the Ideal and Anti-Ideal Solutions:** For each criterion, identify the best (ideal) and worst (anti-ideal) values among all alternatives.

4. **Calculate the Euclidean Distances:** Calculate the Euclidean distance between each alternative and the ideal and anti-ideal solutions. The Euclidean distance represents the similarity or proximity of an alternative to the ideal or anti-ideal solution for each criterion.

5. **Calculate the Relative Closeness to the Ideal Solution:** Determine the relative closeness of each alternative to the ideal solution by comparing the distances. The alternative with the shortest distance is considered the most favorable.

6. **Rank the Alternatives:** Rank the alternatives based on their relative closeness to the ideal solution. The alternative with the highest relative closeness is considered the best choice.

TOPSIS is widely used in various fields such as business, engineering, and environmental studies when there are multiple criteria to consider in decision-making processes. It provides a systematic and quantitative way to analyze and compare alternatives, taking into account multiple criteria simultaneously.


# METHODOLOGY:-

**Sentence Embeddings and Similarity Matrix:**

1. Utilizes a pre-trained model (model, assumed to be a sentence embedding model like BERT, GPT-3, USE, or XLNet) to obtain embeddings for a list of sentences (sentences).
2. Computes the cosine similarity matrix between all pairs of sentences.
3. Creates a DataFrame (df_similarity_matrix) and displays it as a table and heatmap.

**Similarity Scores with a Reference Sentence:**

1. Obtains the sentence embedding for a reference sentence (reference_sentence) and calculates cosine similarity scores between the reference sentence and each of the original sentences.
2. Computes an additional criterion score based on the average length of words in each sentence.

**Score Normalization and Weighted TOPSIS:**

1. Normalizes the cosine similarity scores and additional criterion scores using Min-Max scaling.
2. Assigns weights to the normalized scores and calculates weighted normalized scores.
3. Determines positive and negative ideal solutions.
4. Computes the TOPSIS (Technique for Order of Preference by Similarity to Ideal Solution) score for each sentence.
5. Ranks the sentences based on their TOPSIS scores.

**Visualization and Output:**

1. Displays the ranked models and their TOPSIS scores in a table.
2. Generates a bar chart to visualize the TOPSIS scores.
3. Creates a table (using PrettyTable) summarizing the cosine similarity, additional criterion, and TOPSIS score for each model.

# Models used
1. BERT
2. GPT-3
3. USE
4. XLNet

# Key Findings
<img width="375" alt="image" src="https://github.com/Drishti-17/text_sentence_similarity_using_topsis/assets/91721425/74777a60-31cf-4d6c-afc8-f82ca20d2c4d">


# Final Result
<img width="228" alt="image" src="https://github.com/Drishti-17/text_sentence_similarity_using_topsis/assets/91721425/85f06383-cca8-4842-a77f-205aff71726b">


# Visual Insights 
<img width="594" alt="image" src="https://github.com/Drishti-17/text_sentence_similarity_using_topsis/assets/91721425/f04180d2-20c9-445f-9dcb-60e63914b034">


