# Food Tourism: Personalized Restaurant Recommendations

## Table of Contents
1. Introduction  
2. Business Problem  
3. Stakeholders  
4. Objectives  
5. Business Understanding  
6. Data Understanding  
7. Data Preparation  
8. Exploratory Data Analysis (EDA)  
9. Modeling Approach  
10. Results  
11. Business Impact  
12. Recommendations  
13. Future Improvements  
14. Contributors  
15. License  

---

# Introduction

Savor Space is a tourism and travel company focused on delivering seamless and memorable travel experiences. Beyond accommodation bookings and guided tours, the company recognizes that food experiences are a critical part of tourism.

Travelers often struggle to identify restaurants that match their preferences in unfamiliar destinations. To solve this, Savor Space developed an AI-powered restaurant recommendation system that personalizes restaurant suggestions based on customer preferences, reviews, dietary needs, and location.

The goal was to create a production-ready recommendation engine that improves tourist satisfaction while increasing engagement with the Savor Space platform.

---

# Business Problem

Tourists visiting new destinations frequently rely on random online reviews or generic search rankings when choosing restaurants. This creates several challenges:

- Poor dining experiences caused by irrelevant recommendations  
- Difficulty finding restaurants that meet dietary preferences  
- Information overload from too many options  
- Lower trust in travel platforms that lack personalization  

Savor Space needed a scalable recommendation system capable of delivering accurate, personalized restaurant suggestions in real time.

---

# Stakeholders

### Savor Space Management
Interested in improving customer retention, increasing platform engagement, and boosting ROI through personalized services.

### Tourists / End Users
Primary beneficiaries who receive tailored restaurant recommendations based on their tastes and travel needs.

### Restaurant Owners
Gain increased visibility and traffic when their businesses are recommended to suitable customers.

---

# Objectives

### Primary Goals

1. Build a robust restaurant recommendation engine  
2. Improve tourist dining experiences through personalization  
3. Leverage machine learning and NLP techniques  
4. Optimize recommendation quality using measurable metrics  

### Technical Goals

- Content-Based Filtering  
- Collaborative Filtering  
- Sentiment Analysis  
- Review Text Processing  
- RMSE Optimization  
- Scalable Recommendation Architecture  

---

# Business Understanding

Food is one of the strongest drivers of travel satisfaction. A traveler who enjoys meals aligned with their preferences is more likely to rate their overall trip positively.

For Savor Space, a recommendation engine creates value by:

- Increasing app engagement  
- Building customer loyalty  
- Improving trip satisfaction scores  
- Creating upsell opportunities for tourism packages  
- Strengthening competitive advantage through personalization  

---

# Data Understanding

To develop a real-world recommendation system, restaurant and customer review data were sourced from Yelp.

Five JSON datasets were collected, with two primary datasets used for modeling:

## 1. Business Dataset (`business.json`)

Contains structured restaurant data such as:

- Business name  
- Category  
- Location  
- Ratings  
- Review counts  
- Operational metadata  

## 2. Review Dataset (`review.json`)

Contains user-generated review data including:

- User ratings  
- Text reviews  
- Sentiment indicators  
- User preference signals  

These datasets enabled both structured and unstructured recommendation modeling.

---

# Data Preparation

Data preparation focused on production-quality preprocessing.

## Steps Completed

### Data Cleaning

- Removed duplicates  
- Filtered irrelevant records  
- Standardized missing values  

### Data Transformation

- Converted raw JSON into tabular analytical format  
- Joined business and review datasets  

### Feature Engineering

Created new variables such as:

- Average sentiment score  
- Review frequency  
- Category vectors  
- Combined preference profiles  

### Normalization

Scaled numerical features to prevent dominance during model training.

---

# Exploratory Data Analysis (EDA)

EDA was conducted to identify market patterns and user behavior.

---

## Rating Relationships

A correlation score of **0.41** was found between business ratings and user review ratings.

### Insight:

This indicates a moderate positive relationship, meaning higher-rated restaurants generally receive stronger customer sentiment.

---

## Restaurant Categories

Popular categories dominated the dataset, showing strong demand clusters.

### Insight:

Category concentration helps guide recommendation relevance and market segmentation.

---

## Geographic Distribution

Restaurant availability was uneven across cities.

### Major Markets:

- Philadelphia (highest concentration)  
- Tampa (strong secondary market)  

### Lower Density Markets:

- Edmonton  
- Santa Barbara  

### Insight:

Location density strongly impacts recommendation diversity.

---

## Popular Restaurants

Restaurants with:

- High review volume  
- High average rating  

were consistently top-ranked.

### Insight:

Trust signals matter heavily in customer decision-making.

---

## Review Word Cloud

Frequent positive terms revealed common user priorities:

- Great service  
- Delicious food  
- Friendly staff  
- Nice atmosphere  

### Insight:

Experience quality matters as much as food quality.

---

# Modeling Approach

A multi-model recommendation strategy was implemented.

---

## 1. Content-Based Recommendation System

Used restaurant attributes and review text similarities.

### Method:

- TF-IDF Vectorization  
- Cosine Similarity Matrix  

### Outcome:

Recommended similar restaurants based on customer tastes.

---

## 2. NLP Pipeline

Review text preprocessing included:

- Punctuation removal  
- Stopword removal  
- Tokenization using `RegexpTokenizer()`  
- Stemming using `SnowballStemmer()`  
- TF-IDF using `TfidfVectorizer()`  

This converted text reviews into machine-readable features.

---

## 3. Deep Neural Networks

Keras neural networks were tested for rating prediction.

### Dataset Scale

- Users: **34,497**  
- Restaurants: **3,720**

### Best Neural Model Performance

- Training RMSE: **0.3896**  
- Test RMSE: **1.3671**

---

## 4. Matrix Factorization (Best Model)

SVD delivered the strongest overall performance.

### Final RMSE:

**1.25**

This outperformed neural approaches for recommendation accuracy.

---

# Results

## Key Wins

### Accurate Recommendations

Personalized restaurant suggestions improved relevance.

### Strong Model Benchmark

SVD delivered best predictive performance.

### Real-World Scalability

Hybrid architecture supports deployment into tourism apps.

### Improved User Experience

Users can quickly discover suitable dining options.

---

# Business Impact

If deployed commercially, this system can drive:

- Higher booking retention  
- Increased customer satisfaction  
- Longer platform session time  
- More repeat users  
- Stronger brand loyalty  

For restaurant partners:

- Increased visibility  
- Better customer matching  
- More quality traffic  

---

# Recommendations

## Immediate Next Steps

### 1. User Feedback Loop

Collect click, save, and booking behavior to improve recommendations.

### 2. Dynamic User Profiles

Continuously learn changing customer tastes.

### 3. Hybrid Recommendation Engine

Combine content + collaborative filtering + context signals.

### 4. Geographic Expansion

Extend into new cities and countries.

---

# Future Improvements

## Advanced Roadmap

### Real-Time Personalization

Use live behavior signals.

### Food Delivery Integration

Allow direct ordering or reservation.

### Social Features

Enable users to share reviews and lists.

### Deep Learning Ranking Models

Use embeddings and transformer architectures.

### Time-Aware Recommendations

Breakfast, lunch, dinner, weekend preferences.

---

# Contributors

Developed by:

- Samuel Gathogo  
- Andrew Manwa  
- Elsie Serem  
- Martin Omondi  
- Nancy Maina  

Contributions are welcome through pull requests and collaboration.

---

# License

This project is licensed under the MIT License.