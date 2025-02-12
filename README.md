# Task Extraction and Categorization

## Overview
This project is a Python-based NLP solution that extracts tasks, assigns them to responsible entities, and categorizes them into predefined groups using machine learning. It leverages text preprocessing, named entity recognition, word embeddings, and K-Means clustering.

## Features
- **Text Preprocessing:** Removes special characters and tokenizes sentences.
- **Task Extraction:** Identifies the assigned person and deadline from tasks.
- **Word Embeddings:** Uses Word2Vec to generate embeddings for tasks.
- **Task Categorization:** Clusters tasks into predefined categories (Household, Work, Errands, Miscellaneous) using K-Means.
- **Structured Output:** Displays extracted task details in a structured format.

## Dependencies
Ensure you have the following libraries installed:
```bash
pip install numpy nltk gensim scikit-learn
```
Additionally, download necessary NLTK resources:
```python
import nltk
nltk.download('punkt')
nltk.download('averaged_perceptron_tagger')
```

## Usage
1. **Preprocess Text:** Convert raw text into tokenized sentences.
2. **Extract Tasks:** Identify assigned entities and deadlines.
3. **Train Word Embeddings:** Generate embeddings for clustering.
4. **Categorize Tasks:** Apply K-Means clustering to classify tasks.
5. **View Structured Output:** Print task details with assignments and deadlines.

## Example
```python
text = '''
    Rahul has to buy snacks for all of us.
    She must complete the assignment by tomorrow.
    John should submit the report before 5 PM.
    I need to finish my homework.
    Rahul wakes up early every day. Rahul should clean the room by 5 pm today.'''

sentences = preprocess_text(text)
categorized_tasks = categorize_tasks(sentences)

for task in categorized_tasks:
    print(task)
```

## Output
The script extracts structured tasks like:
```
{'task': 'Rahul should clean the room by 5 pm today.', 'category': 'Household', 'assigned_to': 'Rahul', 'deadline': 'by 5 pm today'}
```

## Future Improvements
- Enhance entity recognition using spaCy or transformers.
- Improve clustering with more advanced NLP techniques.
- Add support for more complex deadline parsing.

## License
This project is open-source and free to use.
