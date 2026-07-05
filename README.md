# 🚗 Car Insurance Claims: Risk Segmentation and Portfolio Analytics

![Tableau](https://img.shields.io/badge/BI_Tool-Tableau-orange.svg)
![Python](https://img.shields.io/badge/Language-Python_/_Pandas-blue.svg)
![Analytics](https://img.shields.io/badge/Domain-Risk_and_Insurance-green.svg)

## 📌 Project Overview and Strategic Objective
In the auto insurance domain, financial sustainability relies heavily on accurately anticipating claims, optimizing premium rates, and mitigating risk exposure. Unchecked claim frequencies and unpredictable payout severities can severely impact an insurance provider's bottom line.

**Objective:** As Lead Data Analyst, I conducted a comprehensive Exploratory Data Analysis (EDA) on a dataset of **7,647 driver records** to uncover operational risk patterns. I translated these insights into an interactive, 5-dashboard data storyboard designed to help Senior Management implement risk-adjusted pricing and optimize financial reserves.

---

## 🔍 Core EDA Questions and Analytical Answers

### 1. Driver Age Profile (`BIRTH`)
* **Finding:** The distribution of car owners is highly concentrated around middle-aged and older demographics. 
* **Outlier Alert:** Extreme outliers exist on both ends (minimum age of 40 and maximum age of 96), indicating a portfolio skewed heavily toward mature drivers.

### 2. Education vs. Affluence (`EDUCATION` vs `INCOME`)
* **Finding:** There is a strong linear correlation between higher academic degrees and average earnings:
  * **PhD Holders:** Highest average income at **$118,009**
  * **Master's Degrees:** **$82,923**
  * **Bachelors Degrees:** **$65,590**
  * **High School Only:** **$39,100**
  * **Less than High School:** **$25,868**
* **Strategic Value:** Higher educational tiers indicate stronger purchasing power for premium coverage types, though they don't automatically imply a reduction in driving risk.

### 3. Vehicle Age vs. Claim Frequency (`CAR_AGE` vs `CLM_FREQ`)
* **Finding:** Surprisingly, vehicle age demonstrates a very weak statistical correlation with claim frequency ($r = -0.029$). Claims are consistently distributed across both newer and older cars. 
* **Strategic Value:** Car age alone cannot be used as a primary standalone metric to predict the likelihood of an accident occurring.

### 4. Payout Severity by Purpose and Gender (`CAR_USE`, `GENDER` vs `CLM_AMT`)
When a claim is filed, usage context and gender present major variance patterns in total loss payouts:
* **Commercial Use (Male):** Highest average payout at **$2,177** (Totaling $3.39M across 1,559 records).
* **Commercial Use (Female):** **$2,006** average payout.
* **Private Use (Female):** **$1,344** average payout (though capturing the highest volume with $4.39M total payout over 3,271 records).
* **Private Use (Male):** Lowest average claim payout at **$844**.

### 5. Car Type Worth and Marital Dynamics (`CAR_TYPE` vs `BLUEBOOK` / `MSTATUS`)
* **Finding:** Vehicle book values are heavily driven by class categories, with **Panel Trucks and Vans** representing the highest commercial market worth. 
* **Demographic Interaction:** Marital status combined with car type choices shows strong household clustering patterns (e.g., married profiles indexing heavily into Minivans and SUVs for family usage).

---

## 📊 Tableau Interactive Storyboard Structure
The portfolio analysis is split into a professional 5-stage dashboard layout inside `Car_Insurance_Claims.twb`:
1. **Driver Demographics Overview:** Tracks age distributions, education-to-income scales, and portfolio counts.
2. **Vehicle Risk Analysis:** Maps vehicle type, vehicle age, and bluebook valuations against claim likelihood.
3. **Claim Behavior and Severity:** Isolates true cost centers by mapping conditional claim payouts across gender and usage types.
4. **Socioeconomic Impact on Claims:** Investigates correlations between professional background, home ownership values, and insurance risks.
5. **Segmentation and Risk Profiling:** Consolidates geographic environments (Urban vs. Rural risk exposure) and clusters high-risk profiles.

---

## 💡 Strategic Executive Recommendations
1. **Implement Urban Risk Surcharges:** Urban drivers exhibit a **4x higher claim frequency (0.94)** compared to rural drivers (0.23). The company should introduce an urban-density risk loading factor to localized premiums.
2. **Differentiate Commercial Utility Tiers:** Commercial vehicle users yield higher average claim severities, with **Panel Trucks ($6,998)** and **Vans ($6,619)** topping active claims. Tiered commercial premium hikes are recommended for these heavy-utility classes.
3. **Optimize Private/Male Group Pricing:** Private-use vehicles operated by male policyholders demonstrate the lowest financial payout profile ($844 average). This segment can be targeted with highly competitive, lower-premium acquisition campaigns to win low-risk market share.

---

## 🛠️ How to Open and Explore the Project
1. Clone the repository locally.
2. Ensure you have **Tableau Desktop** or **Tableau Public** installed.
3. Open `Dashboards/Car_Insurance_Claims.twb` to explore the interactive dashboards, filters, and analytical actions.
OR
visit `https://public.tableau.com/app/profile/yash.rane2721/viz/Car_Insurance_Claims_17723885998140/CarInsuranceClaims`.
