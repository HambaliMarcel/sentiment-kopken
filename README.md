# Sentiment Analysis Kopi Kenangan Cabang Singapore & Malaysia Kenangan LLM OpenAI

This repository contains a Python script to translate and normalize Instagram comments from mixed Malay and English text to English. The script utilizes OpenAI's GPT-3.5 model for text translation and normalization.

## Usage

### Prerequisites

- Python 3.x
- `pip` package manager
- OpenAI API key

### Setup

#### Installation

Install required Python packages:

```bash
pip install pandas openai
```

#### OpenAI API Key

Replace `YOUR_OPENAI_API_KEY` in the script with your actual OpenAI API key.

### Script Execution

#### Upload CSV File

Upload your CSV file containing the Instagram comments using the provided script. Ensure the CSV file contains a column named `Text_Comment` which holds the original comments.

```python
import pandas as pd
import openai
from google.colab import files

# Upload your CSV file containing the comments
uploaded = files.upload()

# Load the CSV file into a DataFrame
df = pd.read_csv(next(iter(uploaded.keys())))
```

#### Translate and Normalize Comments

Define a function `translate_and_normalize_text` that uses the OpenAI GPT-3.5 model to translate and normalize each comment:

```python
# Set your OpenAI API key
openai.api_key = 'YOUR_OPENAI_API_KEY'

# Define a function to translate and normalize text using OpenAI API
def translate_and_normalize_text(text, model='gpt-3.5-turbo'):
    prompt = f"Translate the following Malay and English mixed text to English and normalize it to remove slang, abbreviations, and informal context:\n\n{text}"

    response = openai.ChatCompletion.create(
        model=model,
        messages=[
            {"role": "system", "content": "You are a helpful assistant."},
            {"role": "user", "content": prompt}
        ]
    )

    return response['choices'][0]['message']['content'].strip()

# Apply the translation and normalization function to each comment
df['Normalized_Comment'] = df['Text_Comment'].apply(lambda x: translate_and_normalize_text(x))

# Save the resulting DataFrame to a new CSV file
df.to_csv('normalized_comments.csv', index=False)

# Provide a download link for the new CSV file
files.download('normalized_comments.csv')
```

### Notes

- Ensure your CSV file is formatted correctly and includes the necessary column (`Text_Comment`).
- Adjust the `model` parameter in `translate_and_normalize_text` function if using a different version of OpenAI's models.
- This script is designed for use in environments like Google Colab where files can be uploaded and downloaded interactively.
- For batch processing of comments, consider optimizing the script for performance and handling potential API rate limits.

---

Feel free to modify and extend the script based on your specific requirements and use cases. If you encounter any issues or have suggestions for improvements, please submit them through GitHub issues or contribute directly via pull requests.


This markdown document provides a comprehensive guide for setting up and using your script for Instagram comment translation and normalization using OpenAI GPT-3.5, suitable for inclusion as a README on your GitHub repository.
