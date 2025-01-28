📌 Project: Psychological Scale Analysis

📝 Overview

This project analyzes psychological measurement scales used in various studies to evaluate the impact of meditation programs. The analysis categorizes scales into positive and negative impact groups and visualizes their frequency and usage patterns.

📂 Data Sources

Outcomes_prepared.csv – Contains processed measurement data from psychological studies.

Code_Book.csv – Provides descriptions and metadata for the measurement scales.

📊 Key Findings

1️⃣ Most Frequently Used Scales

Some psychological scales appear significantly more often, indicating their importance in assessing stress, anxiety, and depression.

2️⃣ Top 10 Most Frequently Used Scales

Beck's Depression Inventory II (26 studies)

Perceived Stress Scale - 10 (15 studies)

Positive and Negative Affect Schedule - Positive (11 studies)

Positive and Negative Affect Schedule - Negative (10 studies)

Beck Anxiety Inventory (8 studies)

Center for Epidemiologic Studies Depression Scale (7 studies)

Perceived Stress Scale - 14 (6 studies)

Generalized Anxiety Disorder-7 (6 studies)

Medical Outcomes Short Form (5 studies)

Brief Symptom Inventory-18 Anxiety (5 studies)

3️⃣ Multi-Scale Studies

27 studies used only one scale (32.5%).

28 studies used two scales (33.7%).

12 studies used three scales (14.5%).

7 studies used four scales (8.4%).

1 study used five scales (1.2%).

Identifying commonly used scale combinations helps refine our analysis.

4️⃣ Scale Directionality Matters

Some scales measure a reduction in negative states (e.g., decreased stress or anxiety).

Others assess positive psychological growth (e.g., improved well-being, mood enhancement).

To ensure accuracy, scales are grouped into:

Negative impact scales (higher values = worse state)

Positive impact scales (higher values = improvement)

🔄 Methodology

Data Preprocessing

Loaded and cleaned raw CSV files.

Mapped measurement scales to positive/negative categories.

Exploratory Data Analysis (EDA)

Counted the number of scales per study.

Identified the most frequently used measurement scales.

Data Visualization

A pie chart was created to show the percentage of studies using 1, 2, 3, 4, or more scales.

📌 Next Steps

Use scale categorization to analyze the effects of meditation across different psychological dimensions.

Investigate trends across study groups based on diagnosis.

Improve statistical analysis by normalizing scores across different measurement scales.

🚀 How to Run the Code

Install dependencies:

pip install pandas matplotlib seaborn numpy

Run the script:

python analyze_scales.py

Review the generated visualizations and summary statistics.

📩 Contact

For any questions or suggestions, please reach out to the project maintainers. 🚀
