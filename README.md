# NewsBot Intelligence System

### ITAI 2373 | Natural Language Processing Midterm Project

**Student:** Ashton Smith  
**Project Type:** Individual NLP Project  
**Platform:** Python and Google Colab

## Project Overview

NewsBot is a natural language processing system designed to analyze and organize news articles automatically. The system combines multiple NLP techniques to classify articles, recognize named entities, analyze sentiment, examine language patterns, and generate useful insights.

I developed this project to demonstrate how different NLP techniques can work together to solve real-world information processing problems.

## Project Features

The system integrates all eight NLP modules:

1. **Real-World NLP Applications:** Identifies business use cases for automated news analysis.
2. **Text Preprocessing:** Cleans and normalizes text using tokenization, stop word removal, and lemmatization.
3. **TF-IDF Analysis:** Identifies important words and generates word clouds, bar charts, and heatmaps.
4. **Part-of-Speech Tagging:** Analyzes grammatical patterns across news categories.
5. **Syntax and Semantic Analysis:** Examines sentence structures, dependencies, and relationships.
6. **Sentiment Analysis:** Measures positive, negative, and neutral sentiment.
7. **Text Classification:** Compares classification algorithms and evaluates their performance.
8. **Named Entity Recognition:** Identifies people, organizations, locations, dates, and other important information.

## Dataset

The project uses the [BBC News Classification Dataset on Kaggle](https://www.kaggle.com/competitions/learn-ai-bbc/data).

The original training dataset contained 1,490 labeled articles. After removing 50 duplicate articles, 1,440 articles remained across five categories:

- Business
- Entertainment
- Politics
- Sports
- Technology

The dataset doesn't provide separate publication dates or article headlines. The system uses article excerpts as title substitutes, and time-based analysis is limited.

## Classification Performance

I compared Naive Bayes, Logistic Regression, and Support Vector Machine classifiers, then experimented with feature selection and model parameters.

The best corrected model was **Multinomial Naive Bayes using TF-IDF features**, with an alpha value of 0.1.

| Performance Metric | Result |
|---|---|
| Training Articles | 1,152 |
| Test Articles | 288 |
| Cross-Validation Accuracy | 97.14% |
| Held-Out Test Accuracy | 95.83% |
| Correctly Classified Test Articles | 276 of 288 |

TF-IDF fitting and hyperparameter selection were performed using training data, with the test set held out for final evaluation.

## Final System Testing

I tested the completed NewsBot with seven additional original, fictional news examples.

All five clearly categorized examples were classified correctly. Two additional articles intentionally combined subjects from different categories.

These tests revealed that the system performs well on clearly defined topics but can have difficulty with ambiguous articles. A potential improvement would be supporting multiple category labels.

## Technologies Used

- Python
- Google Colab
- Pandas and NumPy
- NLTK and spaCy
- Scikit-learn
- Matplotlib and Seaborn
- WordCloud
- NetworkX

## How to Run the Project

1. Download the Jupyter notebook (`.ipynb`) from this repository.
2. Open it using [Google Colab](https://colab.research.google.com/).
3. Download the BBC News Classification dataset from Kaggle using the dataset link above.
4. Upload `learn-ai-bbc.zip` into the Colab Files panel without renaming it. The notebook loads `BBC News Train.csv` directly from that ZIP.
5. Run the notebook cells in order, starting with package installation.
6. Review the outputs, visualizations, model evaluations, and final NewsBot testing.

The notebook requires an active Colab session and access to the dataset. Saved outputs are included for reference.

## Challenges and Lessons Learned

Some of the challenges I encountered included missing NLTK resources, classifier compatibility errors, code indentation issues, and combining multiple NLP components into one working system.

One of the biggest lessons I learned was that adding more features doesn't automatically improve model performance. I also learned why separating training and testing data correctly is essential for reliable evaluation.

The project reinforced the importance of understanding why a model produces certain results rather than focusing only on whether the code runs successfully.

## Future Improvements

Potential improvements include multilabel classification, improved handling of ambiguous articles, testing on more recent news datasets, better contextual sentiment analysis, and additional evaluation using real-world articles.

## Project Purpose

This project was completed individually for ITAI 2373 and is included in my GitHub portfolio to demonstrate practical experience with Python, natural language processing, machine learning, data analysis, and troubleshooting.
