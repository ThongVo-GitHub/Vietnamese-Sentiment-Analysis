# Vietnamese Sentiment Analysis for Movie Reviews

An end-to-end **Vietnamese sentiment analysis system** for classifying movie reviews into **Negative, Neutral, and Positive** sentiment.

The project covers web data collection, Vietnamese text preprocessing, exploratory analysis, classical machine-learning baselines, deep-learning models, and PhoBERT-based experimentation.

This project was developed as a **Samsung Innovation Campus 2025 Capstone Project**.

## Project Overview

Vietnamese user reviews contain informal language, abbreviations, repeated characters, slang, and other noisy text patterns that make sentiment classification challenging.

The goal of this project was to build a complete NLP workflow capable of learning sentiment from Vietnamese movie reviews collected from **MoMo.vn**.

```text
MoMo.vn Movie Reviews
        |
        v
Web Crawling
        |
        v
Text Cleaning & Normalization
        |
        v
Exploratory Data Analysis
        |
        v
Class Balancing
        |
        v
Feature Preparation
        |
        +-------------------+
        |                   |
        v                   v
 Classical ML          Deep Learning
        |                   |
        v                   v
TF-IDF Models       CNN / LSTM / PhoBERT
        |                   |
        +---------+---------+
                  |
                  v
          Model Evaluation
                  |
                  v
        Sentiment Prediction
```

## Sentiment Classes

The classification task contains three sentiment classes:

| Label | Sentiment |
|---|---|
| 0 | Negative |
| 1 | Neutral |
| 2 | Positive |

## Objectives

- Collect Vietnamese movie reviews from MoMo.vn
- Clean and normalize noisy Vietnamese text
- Explore sentiment-class distributions
- Handle class imbalance
- Build traditional machine-learning baselines
- Experiment with deep-learning approaches
- Fine-tune PhoBERT for Vietnamese sentiment classification
- Compare models using standard classification metrics
- Select an effective model for final sentiment prediction

## Tech Stack

### Programming & Data Processing

- Python
- Pandas
- NumPy

### Data Collection

- Selenium
- Web crawling

### Machine Learning

- Scikit-learn
- TF-IDF
- Logistic Regression
- Naive Bayes
- Support Vector Machine
- K-Nearest Neighbors
- Random Forest

### Deep Learning / NLP

- TensorFlow / Keras
- CNN
- LSTM
- CNN-LSTM
- Transformers
- PhoBERT

### Evaluation

- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix

### Development

- Jupyter Notebook
- Git
- GitHub

## My Contribution

I led a **5-member team** in developing the project from data collection to model evaluation.

My contributions included:

- Coordinating the overall project workflow
- Collecting Vietnamese movie reviews from MoMo.vn
- Cleaning and normalizing text data
- Handling informal Vietnamese expressions
- Performing exploratory data analysis
- Preparing text features for machine learning
- Experimenting with multiple ML and deep-learning models
- Comparing model performance
- Evaluating the final models using classification metrics

## 1. Data Collection

Movie reviews were collected from **MoMo.vn**.

The crawler extracted information associated with movie-review pages and created a dataset for downstream sentiment analysis.

The data-collection workflow included:

```text
Movie Review Pages
       |
       v
Selenium Crawler
       |
       v
Extract Review Data
       |
       v
Store Dataset
```

## 2. Vietnamese Text Preprocessing

Vietnamese social-media and review text can contain significant noise.

The preprocessing pipeline included operations such as:

- Converting text to lowercase
- Removing unnecessary punctuation
- Cleaning noisy characters
- Normalizing repeated characters
- Handling common Vietnamese abbreviations
- Normalizing informal or teen-code expressions
- Removing irrelevant content
- Preparing text for feature extraction or tokenization

Examples of informal normalization include:

```text
ko  -> không
hok -> không
dc  -> được
cx  -> cũng
iu  -> yêu
siu -> siêu
```

These preprocessing steps help reduce vocabulary noise and make Vietnamese reviews more consistent.

## 3. Exploratory Data Analysis

EDA was performed to better understand the collected reviews before training models.

The analysis included:

- Sentiment-class distribution
- Text statistics
- Review-content exploration
- Class imbalance analysis
- Common words and expressions
- Visualization of processed data

## 4. Classical Machine Learning Baselines

Several traditional machine-learning models were tested to establish baseline performance.

Text reviews were converted into numerical representations such as **TF-IDF features**.

Models experimented with included:

- Logistic Regression
- Naive Bayes
- Support Vector Machine
- K-Nearest Neighbors
- Random Forest

The models were compared using consistent evaluation metrics.

## 5. Deep Learning

The project also explored deep-learning architectures for Vietnamese sentiment classification.

Experiments included models based on:

- CNN
- LSTM
- CNN-LSTM

These approaches were used to learn more complex representations from review sequences compared with traditional TF-IDF models.

## 6. PhoBERT

PhoBERT was evaluated as a Vietnamese pretrained language-model approach.

Instead of relying only on manually engineered text features, PhoBERT provides contextual representations learned from large-scale Vietnamese text.

The project compared PhoBERT with both classical machine-learning and neural-network approaches.

## Model Evaluation

Models were evaluated using:

- **Accuracy**
- **Precision**
- **Recall**
- **F1-score**
- **Confusion Matrix**

The experiments compared traditional ML, deep learning, and transformer-based approaches.

One of the strongest experimental results was achieved by the **CNN-LSTM model**, reaching approximately:

**95.2% classification accuracy**

The result should be interpreted within the dataset split and experimental setup used in this project.

## Experimental Workflow

```text
Clean Reviews
      |
      +-------------------------------+
      |                               |
      v                               v
 TF-IDF Features                Tokenized Sequences
      |                               |
      v                               v
Logistic Regression                  CNN
Naive Bayes                          LSTM
SVM                                  CNN-LSTM
KNN
Random Forest
      |
      +---------------+---------------+
                      |
                      v
                   PhoBERT
                      |
                      v
              Model Comparison
                      |
                      v
             Final Evaluation
```

## Key Learning Outcomes

This project strengthened my understanding of:

- Vietnamese NLP
- Real-world text-data collection
- Web crawling with Selenium
- Text cleaning and normalization
- Handling informal Vietnamese language
- Feature engineering for NLP
- TF-IDF representations
- Machine-learning baselines
- Neural-network text classification
- Transformer-based language models
- Model evaluation and comparison
- Team coordination for an end-to-end AI project

## Challenges

### Informal Vietnamese

Movie reviews often contain:

- slang;
- abbreviations;
- repeated characters;
- spelling variations;
- emojis and punctuation;
- short or ambiguous statements.

These patterns make preprocessing particularly important.

### Class Imbalance

Sentiment datasets may contain significantly more examples of one class than another.

Class distribution was therefore analyzed and balancing strategies were explored before model training.

### Neutral Sentiment

Neutral reviews can be more difficult to classify because their language may overlap with both positive and negative reviews.

## Limitations

The project has several limitations:

- Reviews were collected from a specific online source
- Sentiment labels may contain ambiguity
- Informal Vietnamese language remains difficult to normalize perfectly
- Model performance may change on reviews from different domains
- Dataset-specific performance should not be interpreted as universal Vietnamese sentiment performance

## Future Improvements

Potential improvements include:

- Collecting a larger and more diverse Vietnamese review dataset
- Improving Vietnamese slang and abbreviation normalization
- Performing systematic hyperparameter tuning
- Applying cross-validation where appropriate
- Experimenting with additional Vietnamese pretrained language models
- Performing detailed error analysis by sentiment class
- Adding model explainability
- Building an inference API
- Deploying the model as an interactive web application
- Adding automated training and evaluation pipelines

## Project Background

**Samsung Innovation Campus 2025 — Capstone Project**

Team size: **5 members**

Project focus:

**Natural Language Processing / Machine Learning / Deep Learning / Vietnamese Sentiment Analysis**

## Repository

Clone the project:

```bash
git clone https://github.com/ThongVo-GitHub/Vietnamese-Sentiment-Analysis.git
cd Vietnamese-Sentiment-Analysis
```

## Author

**Võ Minh Thông**

- GitHub: [ThongVo-GitHub](https://github.com/ThongVo-GitHub)
- LinkedIn: [thongvo129](https://www.linkedin.com/in/thongvo129)

---

This project demonstrates an end-to-end Vietnamese NLP workflow from **raw web data to preprocessing, machine-learning baselines, deep learning, transformer experimentation, and model evaluation**.
