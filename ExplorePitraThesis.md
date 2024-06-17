# Thesis Journal: Sentiment Analysis of Kopi Kenangan's Instagram Comments

## Abstract
This thesis aims to conduct sentiment analysis on user comments from Kopi Kenangan's official Instagram posts in Malaysia and Singapore. The objective is to extract insights regarding customer sentiment towards the brand's expansion into these markets. The process involves scraping, preprocessing, and analyzing comments to categorize sentiment (positive, negative, neutral) and assess confidence levels. This journal outlines the steps undertaken from data collection to final result generation.

## 1. Data Scraping and Analysis
### Objective
Collect raw data from Kopi Kenangan's Instagram posts.
### Output
- `ownerProfilePicUrl`: URL to the profile picture of the post owner.
- `ownerUsername`: Username of the post owner.
- `postUrl`: URL of the Instagram post.
- `inputUrl`: URL for input (if applicable).
- `timestamp`: Timestamp of the comment.
- `id`: Unique identifier of the comment.
- `text`: Text content of the comment.

## 2. Preprocess 1: Restructuring Data
### Objective
Organize data into a structured format suitable for analysis.
### Output Format
- `id`: Unique identifier of the comment.
- `username`: Username of the commenter.
- `text_comment`: Text content of the comment.
- `post_url`: URL of the Instagram post.
- `input_url`: URL for input (if applicable).
- `profile_url`: URL to the profile picture of the commenter.
- `timestamp`: Timestamp of the comment.

## 3. Preprocess 2: Text Extraction
### Objective
Focus on extracting only the essential text data for sentiment analysis.
### Output
- `id`: Unique identifier of the comment.
- `text_comment`: Text content of the comment.

## 4. Preprocess 3: Handling Missing Data
### Objective
Clean data by removing missing values, null values, and blank spaces.

## 5. Preprocess 4: Sentiment Direct Classification
### Objective
Identify comments with 100% positive sentiment based on heart emoticons.

## 6. Preprocess 5: Text Normalization
### Objective
Translate and normalize comments to remove slang, abbreviations, and uncommon words or phrases.

## 7. Preprocess 6: Sentiment Analysis
### Objective
Classify sentiment into positive, negative, and neutral categories with confidence scores ranging from 0 to 100%.

## 8. Preprocess 7: Context Alignment
### Objective
Determine if the normalized comment aligns with the topic or if it is off-topic.

## 9. Generating Final Results
### Objective
Compile and present the analyzed data, sentiment classifications, and insights regarding customer sentiment towards Kopi Kenangan's expansion in Malaysia and Singapore.

This structured approach ensures a systematic analysis of Instagram comments, providing actionable insights for Kopi Kenangan's strategic decision-making process. Each step contributes to refining the data and extracting meaningful sentiment indicators, crucial for understanding customer perceptions and preferences in new markets.

---

## Result - Thesis Journal: Sentiment Analysis of Kopi Kenangan's Instagram Comments

### Insight and Important Information

The thesis focuses on sentiment analysis of user comments on Kopi Kenangan's official Instagram posts in Malaysia and Singapore. This analysis provides valuable insights into customer sentiment regarding the brand's expansion into these markets. The process involves the following steps:

1. **Data Collection**
   - Scraping user comments from Instagram posts.
   - Ensuring a representative sample from both Malaysian and Singaporean markets.

2. **Data Preprocessing**
   - Cleaning the data to remove irrelevant information, such as emojis, special characters, and links.
   - Normalizing the text by converting it to lowercase and removing stopwords.

3. **Sentiment Analysis**
   - Categorizing comments into positive, negative, or neutral sentiment.
   - Using machine learning models or natural language processing (NLP) techniques for sentiment classification.

4. **Confidence Level Assessment**
   - Measuring the confidence level of the sentiment categorization.
   - Ensuring the reliability of the sentiment analysis results.

5. **Insights Extraction**
   - Summarizing the overall customer sentiment towards Kopi Kenangan in Malaysia and Singapore.
   - Identifying key trends, common positive and negative themes, and areas for improvement.

### Statistical Measures

1. **Mean (Average)**
   - The mean is the sum of all data points divided by the number of data points.
   - Formula: \( \bar{x} = \frac{1}{n} \sum_{i=1}^{n} x_i \)
   - Example Calculation: If there are 100 comments with sentiment scores, sum all the sentiment scores and divide by 100.

2. **Median**
   - The median is the middle value when the data points are arranged in ascending order.
   - Formula: 
     - For odd \( n \): Median = \( x_{(\frac{n+1}{2})} \)
     - For even \( n \): Median = \( \frac{x_{(\frac{n}{2})} + x_{(\frac{n}{2}+1)}}{2} \)
   - Example Calculation: If there are 100 sentiment scores sorted in ascending order, the median is the average of the 50th and 51st scores.

3. **Mode**
   - The mode is the value that appears most frequently in the data set.
   - Example Calculation: If the sentiment score "positive" appears most frequently among the comments, then "positive" is the mode.

### Margin of Error Calculation (MRE)

The margin of error indicates the degree of uncertainty in the sentiment analysis results.
- Formula: \( E = z \cdot \frac{\sigma}{\sqrt{n}} \)
  - \( z \) is the z-score (from the standard normal distribution).
  - \( \sigma \) is the standard deviation of the sample.
  - \( n \) is the sample size.
- Example Calculation: Assuming 400 comments with a standard deviation of 0.5 and a 95% confidence level (z ≈ 1.96), the margin of error is approximately 0.049 or 4.9%.

### Summary

This study utilizes statistical measures like mean, median, and mode to summarize sentiment data and calculates the margin of error to assess confidence in the results. These insights help understand customer perceptions and guide strategic decisions for Kopi Kenangan's market expansion.

---

## Sentiment Analysis Approach Benchmark

### Approaches in Sentiment Analysis

1. **Lexicon-based Approach**
   - **Description:** Uses a predefined list of words (a dictionary or corpus) with known sentiment scores.
   - **Example Tools:** Vader, TextBlob
   - **How It Works:** The model checks sentiment scores of words in the text against the dictionary and combines them to determine overall sentiment.

2. **Machine Learning-based Approach**
   - **Supervised Learning:**
     - **Description:** Uses labeled training data to train a model.
     - **Example Algorithms:** Naive Bayes, Support Vector Machines (SVM), Random Forests
     - **How It Works:** Learns patterns in training data to predict sentiments of new texts.
   - **Unsupervised Learning:**
     - **Description:** Finds patterns without labeled training data.
     - **Example Algorithms:** Clustering algorithms like K-means
     - **How It Works:** Groups texts and infers sentiment based on these groupings.

3. **Deep Learning-based Approach**
   - **Description:** Uses neural networks (e.g., BERT, GPT) to understand and predict sentiment.
   - **How It Works for Sentiment Analysis:** Considers context and nuances in text for more sophisticated sentiment understanding.

### Our Existing Approach with an LLM GPT

- **Deep Learning-based Approach:**
  - **How It Works for Sentiment Analysis:** LLMs like GPT-4 (which powers ChatGPT) are trained on vast datasets to predict sentiment by understanding context and subtleties in text.

- **Advantages:**
  - **High Accuracy:** Understands context well, leading to accurate sentiment predictions.
  - **Flexibility:** Can be fine-tuned for specific tasks and datasets.
  - **Nuance Handling:** Picks up on subtleties that simpler models might miss.

- **Considerations for Improvement:**
  - **Resource Intensive:** Requires significant computational resources.
  - **Fine-Tuning:** May require specific fine-tuning on sentiment-specific datasets.
  - **Data Quality:** Depends on high-quality, representative training data for optimal performance.

### Recommendations

1. **Evaluate Performance:**
   - Use metrics like accuracy, precision, recall, and F1 score.
   - Use a confusion matrix to identify areas where the model needs improvement.

2. **Consider Fine-Tuning:**
   - Fine-tune LLMs on labeled sentiment datasets for improved performance.

3. **Check Resource Availability:**
   - Ensure adequate computational resources to handle LLMs effectively.

4. **Compare Approaches:**
   - If resource constraints exist, consider simpler lexicon-based or traditional machine learning approaches.

Using an LLM for sentiment analysis leverages advanced methods for understanding customer sentiment, with fine-tuning and evaluation critical for optimal results.
