# Bellabeat Fitbit Case Study

## Project Overview

This project analyzes historical Fitbit smart-device data to identify patterns in physical activity, sleep duration, and wellness tracking. The objective is to understand consumer smart-device usage and develop data-informed marketing recommendations for Bellabeat, a wellness technology company.

The analysis focuses on **Bellabeat Time**, a wellness watch that supports activity, sleep, and stress tracking.

Using Python for data cleaning and statistical analysis and Tableau for data visualization, this case study examines differences in participant activity levels, daily and hourly movement patterns, sleep behavior, and relationships between activity measurements.

The project follows the six phases of the Google Data Analytics process: Ask, Prepare, Process, Analyze, Share, and Act.

## Business Task

**Business Problem:** Bellabeat wants to better understand how consumers use smart devices and identify opportunities to strengthen its marketing strategy. By analyzing historical Fitbit data, the company can explore consumer activity and sleep patterns that may be relevant to Bellabeat Time.

**Business Objective:** Analyze smart-device usage data to identify trends in physical activity, sleep behavior, and wellness tracking. Translate these findings into data-informed marketing recommendations for Bellabeat Time.

### Key Questions

1. What are some trends in smart device usage?
2. How could these trends apply to Bellabeat customers?
3. How could these trends help influence Bellabeat marketing strategy?

### Stakeholders

- **Urška Sršen:** Bellabeat Co-founder and Chief Creative Officer
- **Sando Mur:** Bellabeat Co-founder and Executive Team Member
- **Bellabeat Executive Team:** Evaluates business growth and marketing opportunities
- **Bellabeat Marketing Analytics Team:** Analyzes consumer behavior and develops marketing insights

## Data Sources

The analysis uses the **FitBit Fitness Tracker Data** dataset, publicly available on Kaggle and originally sourced from the Fitabase research dataset.

The data cover two collection periods:

- **Period 1:** March 12 – April 11, 2016
- **Period 2:** April 12 – May 12, 2016

A total of **12 original CSV datasets** were selected, consisting of six dataset types from each collection period.

### Datasets Analyzed

1. **dailyActivity_merged:** Daily steps, distance, activity intensity, sedentary minutes, and estimated calorie expenditure.
2. **hourlySteps_merged:** Hourly step counts used to identify movement patterns throughout the day.
3. **hourlyIntensities_merged:** Hourly activity intensity measurements.
4. **hourlyCalories_merged:** Estimated calorie expenditure recorded hourly.
5. **minuteSleep_merged:** Minute-level sleep observations used to investigate recorded sleep duration and patterns.
6. **heartrate_seconds_merged:** Heart-rate measurements recorded at intervals of several seconds.

Corresponding datasets from the two periods were consolidated after cleaning, duplicate checks, and validation.

### Data Sources and References

- [FitBit Fitness Tracker Data — Kaggle](https://www.kaggle.com/datasets/arashnic/fitbit)
- [Crowd-sourced Fitbit Datasets — Zenodo](https://doi.org/10.5281/zenodo.53894)

**Data Limitations:** The data were collected in 2016 from a relatively small, nonrandom sample of Fitbit users. Participant coverage varies across datasets, and the results should not be generalized to Bellabeat customers without additional research.

---

## Tools and Technologies

| Tool | Purpose |
|------|---------|
| **Python** | Data cleaning, transformation, statistical analysis, and validation |
| **Pandas** | Data manipulation, aggregation, correlation analysis, and CSV exports |
| **NumPy** | Numerical operations and supporting calculations |
| **Jupyter Notebook** | Developing and documenting the Process and Analyze phases |
| **Google Sheets** | Initial dataset inspection and preparation |
| **Tableau Public** | Creating interactive visualizations and dashboards |
| **Google Docs** | Preparing the final data analysis report |
| **GitHub** | Project documentation, version control, and portfolio presentation |

---

## Data Analysis Process

This project follows the six phases of the Google Data Analytics process: **Ask, Prepare, Process, Analyze, Share, and Act**.

### 1. Ask — Define the Business Problem

- Identified the primary business objective: understand consumer smart-device usage and develop marketing recommendations for Bellabeat.
- Selected **Bellabeat Time** as the product of focus.
- Established three key business questions related to usage trends, potential Bellabeat customer applications, and marketing strategy.
- Identified the stakeholders who would use the analytical findings.

### 2. Prepare — Collect and Evaluate Data

- Obtained historical Fitbit data from Kaggle, covering two collection periods in 2016.
- Selected **12 CSV datasets**, representing six dataset types across both periods.
- Inspected dataset dimensions, column structures, data types, missing values, and duplicate observations.
- Evaluated data credibility, completeness, sampling limitations, and potential bias.
- Organized the original datasets for cleaning and analysis.

### 3. Process — Clean and Transform Data

- Used **Python, Pandas, and NumPy** in Jupyter Notebook to clean and consolidate datasets.
- Resolved duplicate records and overlapping observations between collection periods.
- Standardized date and timestamp variables.
- Investigated zero-step observations, zero-calorie records, unusual heart-rate measurements, and irregular sleep durations.
- Created calculated fields and data quality flags.
- Consolidated daily activity data into **1,373 unique participant-day observations**.
- Summarized minute-level sleep observations into **1,007 sleep logs**.
- Exported cleaned datasets for analysis.

### 4. Analyze — Identify Trends and Relationships

- Calculated descriptive statistics for physical activity, estimated calorie expenditure, heart rate, and recorded sleep duration.
- Classified **35 participants** into four activity groups based on average daily steps.
- Investigated hourly movement patterns and differences in activity across days of the week.
- Compared weekday and weekend activity using observation-level and participant-level analyses.
- Conducted Pearson and Spearman correlation analyses.
- Examined the relationship between daily steps and estimated calorie expenditure.
- Performed sensitivity analysis to evaluate the influence of unusual sleep durations.
- Exported and validated **10 analytical summary tables**.

### 5. Share — Visualize and Communicate Findings

- Used **Tableau Public** to create visualizations of the analytical results.
- Developed six supporting visualizations covering:
  1. Participant activity groups
  2. Activity intensity by group
  3. Daily steps by day of week
  4. Hourly step patterns
  5. Recorded sleep duration by day of week
  6. Correlations between activity measurements
- Organized visualizations into a dashboard.
- Documented key findings and supporting statistical tables in the final case study report.

### 6. Act — Develop Business Recommendations

Based on the findings, developed three marketing recommendations for Bellabeat Time:

1. **Promote Personalized Activity Goals:** Highlight individual progress tracking and realistic movement goals for consumers with different activity levels.
2. **Test Routine-Based Activity Messaging:** Explore marketing content and activity reminders informed by daily and weekly movement patterns.
3. **Highlight Comprehensive Wellness Tracking:** Emphasize the value of monitoring multiple wellness measurements, including activity intensity and sleep patterns.

These recommendations are exploratory and should be validated through additional Bellabeat customer research and marketing experiments before implementation.

---

## Key Findings and Insights

### 1. Daily Activity Levels

- Across **1,373 participant-day observations**, the average daily step count was **7,377.38 steps**.
- Of the 35 participants, **57.14%** averaged fewer than 7,500 daily steps.
- Only **20%** of participants averaged at least 10,000 daily steps.
- Participants with higher average step counts generally recorded more very active minutes.

**Business Insight:** Differences in activity levels suggest an opportunity for Bellabeat to explore personalized activity goals rather than promoting a single universal step target.

### 2. Hourly Activity Patterns

- Average hourly steps were lowest during overnight and early-morning hours.
- Activity generally increased throughout the morning and remained elevated during much of the day.
- The highest average hourly step count occurred at **7:00 PM**, with **554.89 steps**.

**Business Insight:** These patterns suggest opportunities to test activity-related messaging and reminders that align with consumers' daily routines.

### 3. Weekly Activity Trends

- **Saturday** recorded the highest average daily steps at **7,752.27**.
- **Sunday** recorded the lowest average daily steps at **6,606.73**.
- The difference between these two days was approximately **1,146 steps**.
- Participant-level comparisons showed approximately **206 fewer steps on weekends** than weekdays, on average.

**Business Insight:** Differences in weekly activity patterns could help Bellabeat explore flexible movement goals and day-specific engagement strategies.

### 4. Recorded Sleep Patterns

- The initial sleep dataset contained **1,007 sleep logs**, with an average recorded duration of **6.34 hours**.
- After excluding **132 logs flagged for unusual durations**, the remaining **875 logs** averaged **6.93 hours**.
- Among unflagged logs, Sunday had the longest average recorded duration at **7.36 hours**, while Saturday had the shortest at **6.68 hours**.

**Business Insight:** Variations in recorded sleep patterns highlight opportunities to explore sleep-tracking summaries, personalized insights, and wellness education.

**Interpretation Note:** Recorded sleep-log duration does not necessarily represent actual time asleep.

### 5. Relationships Between Activity Measurements

Pearson correlation analysis identified several relationships:

| Variable Relationship | Pearson Correlation (r) |
|-----------------------|-------------------------|
| Daily Steps vs. Very Active Minutes | 0.677 |
| Daily Steps vs. Estimated Calories | 0.576 |
| Very Active Minutes vs. Estimated Calories | 0.599 |
| Daily Steps vs. Sedentary Minutes | -0.351 |
| Sedentary Minutes vs. Estimated Calories | -0.111 |

Additional participant-level analysis found:

- **Between-participant steps-calorie correlation:** 0.432
- **Within-participant steps-calorie correlation:** 0.802

The stronger within-participant correlation suggests that days with higher-than-usual step counts generally corresponded to higher-than-usual estimated calorie expenditure for the same participant.

**Business Insight:** Monitoring changes in individual activity measurements over time may offer useful opportunities for personalized wellness tracking.

**Statistical Note:** Correlations describe associations and do not establish causation.

### Overall Interpretation

The analysis identified differences in participant activity levels, daily and weekly movement patterns, recorded sleep duration, and relationships between activity measurements.

These findings suggest potential opportunities for Bellabeat Time to emphasize:

- Personalized activity goals
- Routine-based movement reminders
- Individual progress tracking
- Broader wellness and sleep monitoring

Because the analysis uses historical Fitbit data from a limited sample, these opportunities require additional Bellabeat customer research and validation.

---

## Project Files and Repository Structure

The repository is organized into four main folders containing the final report, Python notebooks, analytical outputs, and Tableau visualizations.

### 1. Documentation

- [Final Bellabeat Case Study Report (PDF)](Documentation/Ivan_Sandoval_Bellabeat_Case_Study.pdf)

The report contains the business task, data sources, cleaning methodology, statistical analysis, supporting visualizations, marketing recommendations, and appendices.

### 2. Python Notebooks

- [Bellabeat Process Phase](Notebooks/Bellabeat_Process.ipynb) — Data cleaning, consolidation, transformation, and validation.
- [Bellabeat Analyze Phase](Notebooks/Bellabeat_Analyze.ipynb) — Descriptive statistics, activity trends, correlation analysis, sensitivity analysis, and analytical exports.

These notebooks document the Python code and analytical methods used throughout the project.

### 3. Analysis Outputs

The [Analysis_Outputs](Analysis_Outputs/) folder contains 10 CSV files generated during the Analyze Phase.

| File | Description |
|------|-------------|
| `activity_groups.csv` | Participant distribution by average daily step category |
| `activity_group_profiles.csv` | Activity and calorie metrics by participant group |
| `weekday_steps.csv` | Average daily step statistics by day of week |
| `hourly_steps.csv` | Hourly step activity summaries |
| `hourly_intensity.csv` | Hourly activity intensity summaries |
| `hourly_calories.csv` | Hourly estimated calorie expenditure |
| `sleep_by_weekday.csv` | Recorded sleep duration statistics by day of week |
| `daily_activity_correlations.csv` | Pearson and Spearman correlation results |
| `key_findings.csv` | Summary of major analytical findings |
| `business_insights.csv` | Analytical findings and potential Bellabeat applications |

### 4. Visualizations

The [Visualizations](Visualizations/) folder contains six Tableau visualization images.

- [Activity Groups](Visualizations/Activity%20Groups.png)
- [Activity Group Profiles](Visualizations/Activity%20Group%20Profiles.png)
- [Weekday Steps](Visualizations/Weekday%20Steps.png)
- [Hourly Steps](Visualizations/Hourly%20Steps.png)
- [Sleep by Weekday](Visualizations/Sleep%20by%20Weekday.png)
- [Activity Correlations](Visualizations/Activity%20Correlations.png)

These visualizations support the main findings presented in the final report.

### Data Availability

The original Fitbit datasets are publicly available through Kaggle and Zenodo.

Large original and cleaned datasets are not stored in this repository. Instead, the repository provides the analysis notebooks, summarized analytical outputs, supporting visualizations, and final report.

---

## Interactive Tableau Dashboard

The analytical findings were visualized using Tableau Public to explore patterns in physical activity, sleep duration, and relationships between wellness measurements.

**[View the Bellabeat Case Study Dashboard on Tableau Public](https://public.tableau.com/views/BellabeatCaseStudyActivitySleepInsights_17917078616110/BellabeatDashboard)**

### Dashboard Visualizations

The project includes six supporting visualizations:

1. **Activity Groups:** Distribution of participants by average daily steps.
2. **Activity Group Profiles:** Comparison of activity intensity across participant groups.
3. **Weekday Steps:** Average daily steps across the seven days of the week.
4. **Hourly Steps:** Movement patterns throughout the 24-hour day.
5. **Sleep by Weekday:** Average recorded sleep duration across the week.
6. **Activity Correlations:** Relationships between daily steps, activity intensity, sedentary time, and estimated calories.

These visualizations complement the statistical analyses and help communicate findings to Bellabeat stakeholders.

---

## References

- **Kaggle:** [FitBit Fitness Tracker Data](https://www.kaggle.com/datasets/arashnic/fitbit)
- **Zenodo:** [Crowd-sourced Fitbit Datasets, 2016](https://doi.org/10.5281/zenodo.53894)

### Project Disclaimer

This is an independent educational case study developed for data analytics portfolio purposes.

The analysis uses historical Fitbit data and does not represent actual Bellabeat customer research. All business recommendations are exploratory and would require additional validation before implementation.
