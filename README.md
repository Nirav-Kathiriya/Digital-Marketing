# The Role of Data Science in Digital Marketing

MSc Data Science project · Leeds Beckett University, UK · Nirav Kathiriya

## Business question
Which campaign choices (campaign type, target audience and channel) drive a marketing campaign's **conversion rate**, and can we predict conversion before a campaign runs?

## Data
- **Marketing Campaign Performance dataset**: 200,000 campaigns × 16 columns. It covers company, campaign type, target audience, duration, channel, conversion rate, acquisition cost, ROI, location, language, clicks, impressions, engagement score, customer segment and date.
- Public dataset from Kaggle. It is not included here because of its size. Download it as `marketing_campaign_dataset.csv` and place it next to the notebook.

## What I did
1. **Data cleaning**: checked missing values and duplicates (none), converted dates, stripped `$` and `,` from acquisition cost, and turned "30 days" into numbers.
2. **Exploratory analysis**: looked at the campaign type mix, the conversion rate distribution, impressions vs clicks by audience, campaigns per channel, and a correlation heatmap.
3. **Modelling**: label-encoded the categories and compared **Random Forest**, **Decision Tree** and **Linear Regression** models that predict conversion rate (80/20 train/test split).

## Key findings
- The data is very evenly spread: each of the 5 campaign types makes up about 20% of campaigns, and conversion rates range from 1% to 15% (average 8%).
- All three models scored an **R² of about 0**. This means campaign type, audience and channel **on their own do not explain conversion rate** in this data.
- **What this means for a marketing team:** choosing a channel or campaign type is not enough to lift conversions. The next things to test are factors like creative, offer and timing, and engagement features such as clicks and engagement score.

## Tools
Python · Pandas · NumPy · Matplotlib · Seaborn · Scikit-learn · Jupyter

## Files
| File | What it is |
|---|---|
| `notebooks/marketing_campaign_analysis.ipynb` | Full analysis: cleaning, EDA, charts and models |
| `report/Data_Science_in_Digital_Marketing_Nirav_Kathiriya.pdf` | Written report: introduction, literature review and methodology (33 pages) |

## How to run
```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
jupyter notebook notebooks/marketing_campaign_analysis.ipynb
```
