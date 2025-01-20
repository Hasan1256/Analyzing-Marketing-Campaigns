# Marketing Campaign Analysis with Pandas

## Project Overview
This project focuses on analyzing marketing campaigns to identify patterns, measure effectiveness, and resolve inconsistencies in campaign performance. Using Python and pandas, the project explores key metrics such as conversion rates, retention rates, and the impact of language preferences on campaign success. The dataset provides insights into user interactions, campaign details, and subscription outcomes.

---

## Dataset Details
The dataset includes information about marketing campaigns and user interactions. Below are the key columns:

- **user_id**: Unique identifier for each user.
- **date_served**: Date the campaign was served.
- **marketing_channel**: Channel used for the campaign (e.g., House Ads, Instagram, Facebook).
- **converted**: Indicates whether the user converted (True/False).
- **language_displayed**: Language of the campaign.
- **language_preferred**: User's preferred language.
- **age_group**: Age group of the user.
- **date_subscribed**: Date the user subscribed (if applicable).
- **date_canceled**: Date the subscription was canceled (if applicable).
- **subscribing_channel**: Channel through which the user subscribed.
- **is_retained**: Indicates whether the user retained their subscription (True/False).

### Notes:
- **Missing Values**: Some columns (e.g., `date_canceled`) have missing values representing retained users or unserved campaigns.
- **Derived Features**:
  - `channel_code`: Numeric encoding of subscribing channels.
  - `is_correct_lang`: Indicates whether the campaign was served in the user's preferred language.
  - `DoW`: Day of the week derived from `date_served`.

---

## Key Questions Explored

1. **Does a mismatch between `language_displayed` and `language_preferred` impact conversion rates?**
   - Analyzed conversion rates for users shown ads in their preferred language versus non-preferred language.

2. **Which marketing channels perform the best?**
   - Calculated and compared conversion rates and retention rates across channels.

3. **How does the day of the week affect campaign performance?**
   - Visualized daily marketing reach and trends in conversions by `DoW`.

4. **What are the key features associated with higher retention rates?**
   - Explored how language preference, age group, and subscribing channels impact user retention.

5. **Do cultural differences impact the effectiveness of campaigns?**
   - Analyzed conversion rates by language over time to identify patterns and cultural influences.

---

## Project Highlights

### Metrics and Calculations:
- **Conversion Rate**:
  - Percentage of users who subscribed after being served a campaign.
- **Retention Rate**:
  - Percentage of users who retained their subscription after conversion.
- **Daily Marketing Reach**:
  - Count of unique users served per channel each day.

### Visualizations:
1. **Conversion Rate by Language**:
   - Bar charts comparing conversion rates for different languages.
2. **Daily Marketing Reach**:
   - Line charts showing user interactions over time across channels.
3. **Retention Rate Trends**:
   - Visualized patterns in retention rates across channels and age groups.
4. **Cultural Analysis**:
   - Analyzed the impact of language and cultural differences on campaign effectiveness.

### Inconsistencies Resolved:
1. **Conversion Data**:
   - Identified and resolved conflicting `converted` values for duplicate records.
2. **Language Mismatch**:
   - Highlighted and addressed inconsistencies between `language_displayed` and `language_preferred`.
3. **Retention Trends**:
   - Analyzed and corrected patterns where retention data appeared inconsistent or incomplete.

---

## Key Functions in the Project

- **Conversion Function**:
  - A utility function to calculate conversion rates for any subset of the dataset.
- **Retention Analysis**:
  - Functions to analyze retention rates by channel, age group, and language.
- **Language Impact Analysis**:
  - Functions to compare conversion rates and trends by language over time.

---

## Installation and Usage

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-repository-name.git
   cd marketing-campaign-analysis
   ```

2. **Install Dependencies**:
   Install the required Python libraries:
   ```bash
   pip install pandas matplotlib numpy
   ```

3. **Run the Notebook**:
   Open and execute the Jupyter Notebook:
   ```bash
   jupyter notebook Marketing_Campaign_Analysis.ipynb
   ```

---

## Results

- **Language Mismatch**: Users served ads in their preferred language showed significantly higher conversion rates.
- **Channel Performance**: Instagram had the highest conversion rates, while Facebook showed steady retention trends.
- **Cultural Insights**: Cultural differences impacted the effectiveness of campaigns; tailored campaigns improved conversions.

---

## Future Work

1. Automate anomaly detection for inconsistencies in conversion and retention data.
2. Integrate machine learning models for predicting user retention and campaign success.
3. Expand the analysis to include time-series forecasting for campaign planning.

---

## License

This project is licensed under the MIT License.
