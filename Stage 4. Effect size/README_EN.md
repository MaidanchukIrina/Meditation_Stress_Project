# 🧘‍♀️ The Impact of Meditation on Psychological Well-Being

## 📁 Raw Dataset Overview

This part of project explores the psychological effects of meditation using real-world data from a published meta-analysis.  
The raw dataset includes results from dozens of studies evaluating participants' emotional states before and after meditation practices.

📊 The original dataset contains:

- Over **50 different psychological scales** (e.g., PSS, BDI, PANAS, BAI)
- **Separate mean values** for treatment (meditation) and control groups:
  - `e_tmean` = treatment group mean
  - `e_cmean` = control group mean
- **Standard deviations** for each group:
  - `e_tsd`, `e_csd`
- **`e_time`**: number of weeks from the start of the study until the measurement
- Additional technical fields like adjusted means, effect sizes, confidence levels

📌 While comprehensive, this format required restructuring to be analysis-ready.

---

## 🧩 The Problem

The raw format followed a **"wide" structure**, with different columns for each group's data.  
Moreover, not all scales interpret results in the same direction — for some, lower scores indicate improvement (e.g., depression), while others indicate improvement through higher scores (e.g., positive affect).

---

## 🎯 Goal

To build a **clean and unified core dataset** that allows for:

- Filtering by psychological scale
- Comparing treatment vs control groups
- Tracking changes over time
- Easy integration with Python libraries, Tableau, or Power BI

---

## ✅ Selected Scales for Core Analysis

After analyzing the frequency and consistency of the scales, I selected the following six, which:

- Are commonly used across studies
- Measure **negative emotional states**, where **lower scores = improvement**
- Allow consistent visual and statistical interpretation

🧠 Selected Scales:

| Scale Name | What It Measures                 |
|------------|----------------------------------|
| BDI-II     | Depression                        |
| PSS-10     | Perceived stress (10-item scale) |
| PSS-14     | Perceived stress (14-item scale) |
| PANAS-n    | Negative affect (emotions)       |
| BAI        | Anxiety                          |
| CES-D      | Depressive symptoms              |

📌 *Note:* The positive emotions scales types was excluded from the core dataset and will be analyzed separately as an indicator of increased psychological resources (rather than reduced distress).

---

## 🔧 Transformation: From Raw Data to Core Dataset

### Raw Columns:
- `e_tmean`, `e_cmean`: mean scores for treatment and control groups
- `e_time`: weeks since start of study
- `o_short`: name of the psychological scale used

### Long Format Transformation

To simplify analysis and visualization, I converted the dataset from **wide to long format**:

- Combined both group means into a single `mean_score` column
- Created a new `group` column to indicate `treatment` or `control`