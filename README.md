# Sentiment-Kopi Kenangan
Aims to conduct sentiment analysis on user comments from Kopi Kenangan's official Instagram posts in Malaysia and Singapore. Involves scraping, preprocessing, and analyzing comments to categorize sentiment (positive, negative, neutral) and assess confidence levels.

## **1. Data Scraping and Analysis**
Objective: Collect raw data from Kopi Kenangan's Instagram posts.
Output:
`ownerProfilePicUrl`: URL to the profile picture of the post owner.
`ownerUsername`: Username of the post owner.
`postUrl`: URL of the Instagram post.
`inputUrl`: URL for input (if applicable).
`timestamp`: Timestamp of the comment.
`id`: Unique identifier of the comment.
`text`: Text content of the comment.

## **2. Preprocess 1: Restructuring Data**
Objective: Organize data into a structured format suitable for analysis.
Output Format:
`id`: Unique identifier of the comment.
`username`: Username of the commenter.
`text_comment`: Text content of the comment.
`post_url`: URL of the Instagram post.
`input_url`: URL for input (if applicable).
`profile_url`: URL to the profile picture of the commenter.
`timestamp`: Timestamp of the comment.

## **3. Preprocess 2: Text Extraction**
Objective: Focus on extracting only the essential text data for sentiment analysis.
Output:
`id`: Unique identifier of the comment.
`text_comment`: Text content of the comment.

## **4. Preprocess 3: Handling Missing Data**
Objective: Clean data by removing missing values, null values, and blank spaces.

## **5. Preprocess 4: Sentiment Direct Classification**
Objective: Identify comments with 100% positive sentiment based on heart emoticons.

## **6. Preprocess 5: Text Normalization**
Objective: Translate and normalize comments to remove slang, abbreviations, and uncommon words or phrases.

## **7. Preprocess 6: Sentiment Analysis**
Objective: Classify sentiment into positive, negative, and neutral categories with confidence scores ranging from 0 to 100%.

## **8. Preprocess 7: Context Alignment**
Objective: Determine if the normalized comment aligns with the topic or if it is off-topic.

## **9. Generating Final Results**
Objective: Compile and present the analyzed data, sentiment classifications, and insights regarding customer sentiment towards Kopi Kenangan's expansion in Malaysia and Singapore.


This structured approach ensures a systematic analysis of Instagram comments, providing actionable insights for Kopi Kenangan's strategic decision-making process. Each step contributes to refining the data and extracting meaningful sentiment indicators, crucial for understanding customer perceptions and preferences in new markets.



