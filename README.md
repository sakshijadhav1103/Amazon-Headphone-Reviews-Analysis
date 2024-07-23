# Amazon-Headphone-Reviews-Analysis
This project involves scraping, analyzing, and deriving insights from Amazon customer reviews of three headphone brands: Sony, JBL, and Boat. Using Python and NLTK, we scraped 589 reviews. The analysis includes sentiment analysis, ANOVA tests to assess brand influence on sentiments, and logistic regression to predict brands based on sentiments.

## Data Collection

### Scraping Reviews
The reviews were scraped using Python's `requests` and `BeautifulSoup` libraries. We extracted the following information for each review:
- Rating
- Title
- Body
- Place and Date of Review

The scraping was performed for three products:
- **JBL Tune 710BT**: [Amazon Link](https://www.amazon.in/JBL-Playtime-Charging-Headphones-Assistant/product-reviews/B096G2RN6D/ref=cm_cr_arp_d_viewopt_srt?ie=UTF8&reviewerType=all_reviews&sortBy=recent&pageNumber=1)
- **Sony WH-CH510**: [Amazon Link](https://www.amazon.in/SONY-WH-CH510-Wireless-Headphone-Blue/product-reviews/B0817T8FB6/ref=cm_cr_arp_d_viewopt_srt?ie=UTF8&reviewerType=all_reviews&sortBy=recent&pageNumber=1)
- **boAt Rockerz 558**: [Amazon Link](https://www.amazon.in/boAt-Rockerz-558-Bluetooth-Headphones/product-reviews/B0BVRGZ9FV/ref=cm_cr_arp_d_viewopt_srt?ie=UTF8&reviewerType=all_reviews&sortBy=recent&pageNumber=1)

### Data Storage
The reviews were saved into CSV files:
- `JBLreviews.csv`
- `Sonyreviews.csv`
- `Boatreviews.csv`

  ## Data Preprocessing

### Cleaning
The data was cleaned to ensure consistency. This included:
- Converting ratings to float
- Extracting country information from the place and date of review
- Removing null values

### Sentiment Analysis
Using NLTK's SentimentIntensityAnalyzer, sentiment scores (negative, neutral, positive, and compound) were computed for each review body.

## Exploratory Data Analysis (EDA)
The EDA focused on:
- Distributions of ratings and sentiments
- Comparisons of sentiment scores across different products

## Statistical Analysis

### MANOVA
A Multivariate Analysis of Variance (MANOVA) was conducted to assess if there are significant differences in sentiment scores (neg, neu, pos, comp) between different products.

### ANOVA
ANOVA analyses were conducted for each sentiment score to further investigate the impact of the product on sentiment.

### Tukey's HSD Test
Post-hoc Tukey's Honestly Significant Difference (HSD) tests were performed to identify specific group differences.

## Predictive Modeling

### Logistic Regression
A logistic regression model was implemented to predict the product based on sentiment scores. The model was tuned using GridSearchCV and evaluated using cross-validation.



  
  
