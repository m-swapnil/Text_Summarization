# Text Summarization

This project implements text summarization using Python. It demonstrates how to process and summarize large text documents effectively by identifying the most relevant sentences. The approach leverages text preprocessing, tokenization, frequency-based scoring, and sentence ranking to generate concise summaries.

---

## Features

- Tokenizes input text into sentences and words.
- Cleans the text by removing stopwords and punctuation.
- Calculates word frequencies while excluding overly common or rare words.
- Scores sentences based on word importance.
- Extracts the most significant sentences to form a summary.
- Computes word counts before and after summarization.

---

## Prerequisites

Ensure the following are installed:

- **Python 3.7 or above**
- Required libraries:
  ```bash
  pip install nltk
  ```

---

## File Structure

```plaintext
.
|-- text_summarization.py   # Main script for text summarization
|-- Lordoftherings.txt      # Input text file to summarize
```

---

## Script Workflow

### 1. **Text Preprocessing**
- Converts text to lowercase for uniformity.
- Tokenizes text into sentences and words using `nltk`.
- Removes stopwords and punctuation.

### 2. **Frequency Analysis**
- Calculates normalized word frequencies.
- Filters out words that are overly common or rare using predefined thresholds.

### 3. **Sentence Scoring**
- Scores each sentence by summing the frequencies of its words.
- Ranks sentences by their scores.

### 4. **Summarization**
- Extracts the top `N` sentences (configurable) as the summary.
- Provides word counts before and after summarization.

---

## Configuration

1. **Input File**
   - Place the text file (e.g., `Lordoftherings.txt`) in the working directory.
   - Update the file path in the script if necessary:
     ```python
     with open("C:/path/to/your/file.txt", 'r', encoding='utf-8') as file:
     ```

2. **Adjust Parameters**
   - Change `num_sentences` in the `summarize` function to control the summary length:
     ```python
     summarize(lor, num_sentences=3)
     ```

---

## Usage

1. **Run the Script**
   ```bash
   python text_summarization.py
   ```

2. **Output**
   - Total sentences in the input text.
   - Summary for the top 1, 3, or more sentences.
   - Word counts before and after summarization.

---

## Example Output

For the provided `Lordoftherings.txt` file:

```
Total Sentences: 21
Summary (3 sentences): ['Sentence 1', 'Sentence 2', 'Sentence 3']
Summary (1 sentence): ['Sentence 1']
Word Count Before Summarization: 500
Word Count After Summarization: 75
```

---

## License

This project is licensed under the MIT License.
