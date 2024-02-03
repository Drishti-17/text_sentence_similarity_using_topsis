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

# TEXT SENTENCE SIMILARITY:-

![bJMue](https://github.com/Drishti-17/sentence_similarity_using_topsis/assets/91721425/dcc39252-2039-4da4-97e9-0d45117671d4)


Text sentence similarity refers to the measurement of how similar two or more sentences are in terms of their meaning, content, or structure. This is a crucial aspect in natural language processing (NLP) and information retrieval, as it helps systems understand and quantify the similarity between textual content.

There are various methods and techniques for assessing sentence similarity, and they can be broadly categorized into:

**Lexical Similarity:**

1. Word Overlap: Measures the similarity based on the common words between sentences.
2. Jaccard Similarity: Calculates the similarity as the intersection divided by the union of the words in the sentences.
   
**Semantic Similarity:**

1. Word Embeddings: Utilizes word embeddings (such as Word2Vec, GloVe, or fastText) to represent words in a continuous vector space. Sentence similarity is then computed based on the similarity of the word embeddings.
2. Sentence Embeddings: Represents entire sentences as vectors, capturing their semantic meaning. Methods like Universal Sentence Encoder or BERT embeddings fall into this category.
   
**Syntactic Similarity:**

1. Tree Kernels: Analyzes the sentence structure using parse trees to measure similarity.
2. Dependency Parsing: Examines the relationships and dependencies between words in sentences.
   
**Combination of Approaches:**
Some methods combine both lexical and semantic features to provide a more comprehensive similarity measure.

Several similarity metrics, such as cosine similarity, Euclidean distance, or Pearson correlation, can be applied to quantify the degree of similarity between sentences.

The choice of method depends on the specific requirements of the application. For instance, in information retrieval, you might want to find documents or sentences that are semantically similar to a given query. In machine learning tasks like text classification or clustering, sentence similarity can also be a useful feature.

In summary, text sentence similarity plays a crucial role in various NLP applications, aiding in tasks such as duplicate detection, information retrieval, summarization, and question-answering systems.

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
