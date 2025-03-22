# Text Analysis and Sentiment Scoring Project

## 📋 Project Overview
This project analyzes articles from websites to determine various text metrics and sentiment scores. The analysis includes:
- Sentiment analysis (positive/negative scores and polarity)
- Readability assessment (Fog Index)
- Text complexity metrics (complex word percentage)
- Sentence structure analysis (average sentence length)

## 🔍 Features
- Web scraping articles from provided URLs
- Text preprocessing and cleaning with stop words removal
- Sentiment analysis using positive/negative word dictionaries
- Readability metrics calculation
- Interactive data visualizations
- Comprehensive insights summary

## 📊 Visualizations
The project generates several visualizations:
- Sentiment distribution and correlation plots
- Readability metrics analysis
- Top articles by word count
- Correlation matrix of text metrics
- Summary dashboard of key findings

## 🛠️ Requirements
- Python 3.6+
- Dependencies:
  - pandas, numpy
  - matplotlib, seaborn
  - requests, BeautifulSoup4
  - NLTK
  - fake_useragent
  - tqdm (for progress tracking)

## 🔧 Installation
```bash
# Clone the repository
git clone https://github.com/yourusername/text-analysis-project.git
cd text-analysis-project

# Create and activate virtual environment (optional but recommended)
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt
```

## 📁 Project Structure
```
text-analysis-project/
├── main.py                    # Main script for text analysis
├── StopWords_Generic.txt      # List of stop words to be filtered
├── positive-words.txt         # Dictionary of positive sentiment words
├── negative-words.txt         # Dictionary of negative sentiment words
├── Input.xlsx                 # Input file with URLs to analyze
├── Output.xlsx                # Final output with calculated metrics
├── DetailedAnalysis.csv       # Detailed analysis including text content
├── TextAnalysisInsights.csv   # Key insights from the analysis
└── visualizations/            # Generated visualization images
    ├── sentiment_analysis.png
    ├── readability_analysis.png
    ├── top_articles_by_length.png
    ├── metrics_correlation.png
    └── analysis_summary.png
```

## 🚀 Usage
1. Prepare an Excel file named `Input.xlsx` with a column named "URL" containing article URLs to analyze
2. Ensure the dictionary files (StopWords_Generic.txt, positive-words.txt, negative-words.txt) are in the project directory
3. Run the script:
```bash
python main.py
```
4. Check the output files (Output.xlsx, DetailedAnalysis.csv) and visualization images

## 📈 Methodology
The analysis follows these methodological steps:

### 1. Text Preprocessing
- Web scraping to extract article content
- Tokenization using regular expressions
- Stop words removal for more accurate analysis

### 2. Sentiment Analysis
- Positive score: Count of words matching the positive dictionary
- Negative score: Count of words matching the negative dictionary
- Polarity score: (Positive - Negative) / (Positive + Negative + 0.000001)

### 3. Readability Metrics
- Average sentence length calculation
- Complex word identification based on vowel patterns
- Fog Index: 0.4 * (Average Sentence Length + Percentage of Complex Words)

### 4. Data Visualization
- Distribution plots for sentiment and readability metrics
- Correlation analysis between different text features
- Comparative analysis of articles

## 🔄 Key Components
- `tokenizer()`: Tokenizes text and removes stop words
- `positive_score()` & `negative_score()`: Calculate sentiment scores
- `complex_word_count()`: Identifies complex words in text
- `fog_index()`: Calculates text readability
- `scrape_articles()`: Extracts article content with error handling and retries

## ⚠️ Known Issues
- The base directory path needs to be adjusted based on your file structure
- Web scraping may sometimes fail for certain websites due to robots.txt restrictions
- Performance may be slow for large numbers of articles due to polite scraping practices

## 🔮 Future Enhancements
- Add support for additional languages
- Implement machine learning-based sentiment analysis
- Create an interactive dashboard for results
- Add caching for previously scraped articles
- Improve error handling and logging

## 📝 License
This project is licensed under the MIT License - see the LICENSE file for details.

## 🙏 Acknowledgements
- Black Coffer for the project inspiration
- NLTK project for NLP resources
- Various open-source sentiment dictionaries
