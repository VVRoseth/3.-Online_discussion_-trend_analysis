# Project 3

## College Education & Career Building:
#### Using Natural Language Processing to understand the perceptions of Reddit users
n

**Problem statement:**

Pursuing a college education degree is expensive. It does require an important investment of money, time and effort. Such investment is expected to deliver returns in the form of salaries, benefits and an overall improved standing on the labor market. But the returns to the investment put into acquiring a college are far from guaranteed. At the same time, for those who cannot afford to make such investment, the lack of a degree is perceived as a limitation for a fulfilling career. In this project I aim to answer the following question: Is college education a must-have to build a career and grow professionally?

Reddit can help address this question only partially for mainly two reasons. First, its content is highly subjective. It does not correspond to corroborated facts or sound analyses. It is therefore only useful to understand the perceptions of people but not any relation between college degrees and career. Second, the data suffers from self-selection bias. It captures the opinions and thoughts of those who choose to use Reddit, join a subreddit and participate actively. For these reasons, I will use the Reddit data to answer the following question:

 **--Do the concerns of users in both subreddits overlap to the extent that they cannot be distinguished?--**

 **Methodology:**

Tho address this question, I have selected two subreddits: career guidance and higher education. The analysis was completed in five steps:
1. Data gathering: Data was gathered from two subreddits using Pushshift's API. A total of 10 thousand posts were gathered from each subreddit.

2. Data exploring: The initial data included about 40 variables and 20,000 values. An initial preselection of 16 variables was used to identify the nature of both subreddits and identify irrelevant content.  

3. Data cleaning: In this step duplicates were removed, null values were imputed, serial posters (those who have posted more than 100 times) were deleted, and 8 variables were dropped.

4. Data packing: The final dataset had 19,028 posts and 8 variables.

5. Modeling: Three models were performed to classify the posts into one of the two subreddit categories by using the text in the title of the post and its body.

**Models:**

The baseline accuracy score of the data was 0.519. In other words, prior to modeling the data, I could classify 51.9% of the posts into the career guidance subreddit and I would be right.

I chose three models to classify the data: a Logistic Regression, a Multinomial Naive Bayes, and a Random Forest. Below are the accuracy scores for each of these models:

|Model|Train Score|Test Score|
|-----|-----------|----------|
|Logistic Regression|0.9702|0.9332|
|Multinomial Naive Bayes|0.9544|0.926|
|Random Forest| 0.844 |0.8379|

**Conclusions:**
Looking again at the research question, **do the concerns of users in both subreddits overlap to the extent that they cannot be distinguished?**, the answer is no.

After looking at more than 19,000 posts, each model correctly classified more than 83% of them. This means that the concerns of users in the higher education subreddit have little overlap with the concerns of those looking for career advice.

**How to navigate the files in this repository**:
This readme accompanies five Jupyter Notebooks, 3 data frames, and two versions of a presentation. Below is a brief explanation of each:

- Jupyter notebooks: They contain the code used to collect (notebook 1), analyze (notebook 2) and model (notebook 'Model') data.

- Data frames: There are two separate data frames with the full, unprocessed, information gathered for each subreddit. The third data frame has the clean data used to perform models.

- Presentation: They are identical, the original is in Microsoft Power Point and there is a PDF copy to ensure access of computers that do not have Microsoft Office.
