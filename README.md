# Data Analytics Portfolio — Jocelin Helsa

Hi, I'm Jocelin, a data analyst with a background in Actuarial Science and experience in end-to-end quantitative analysis for research consulting and nonprofit (MEL) projects.

This portfolio collects my end-to-end analytics projects. Each one starts from a real business problem, works through data cleaning and validation, analysis and modelling, and ends with findings and recommendations that a non-technical manager could act on.

📧 celinhelsa28@gmail.com · 💼 [LinkedIn](https://www.linkedin.com/in/jocelin-helsa-418092264) · 🎓 [Certificates](https://github.com/celynhs/Portfolio-Certificate)

---

## Projects at a glance

| Project | Business area | Python | SQL | Power BI | Repository |
|---|---|:---:|:---:|:---:|---|
| [Motor Insurance Pricing: Risk Modelling and Cross-Subsidy](#1-motor-insurance-pricing-risk-modelling-and-cross-subsidy) | Finance / Risk | ✅ | | ✅ | [Insurance-Analysis](https://github.com/celynhs/Insurance-Analysis) |
| [HR Analytics: Workforce, Turnover and Attrition Risk](#2-hr-analytics-workforce-turnover-and-attrition-risk) | Human Resources | ✅ | ✅ | | [HR-Analytics](https://github.com/celynhs/HR-Analytics) |
| [E-commerce Sales Analysis](#3-e-commerce-sales-analysis) | Sales / Marketing | ✅ | | | [Sales-Analysis](https://github.com/celynhs/Sales-Analysis) |

**Skills shown across the projects:** data cleaning and validation · exploratory and statistical analysis · hypothesis testing and effect sizes · regression and GLMs · machine learning (logistic regression, gradient boosting) · customer and risk segmentation · cost and scenario simulation · dashboard design and DAX · turning analysis into business recommendations

---

## 1. Motor Insurance Pricing: Risk Modelling and Cross-Subsidy

![Power BI dashboard: Portfolio Overview](https://raw.githubusercontent.com/celynhs/Insurance-Analysis/main/images/pbi_page1.png)

**Tech stack:** Python (pandas, NumPy, SciPy, statsmodels, scikit-learn, Matplotlib) · Power BI (Power Query, DAX, star schema data model)

**Repository:** [github.com/celynhs/Insurance-Analysis](https://github.com/celynhs/Insurance-Analysis)

### What the project is about
A pricing analysis of 678,013 French motor insurance policies, approached as a pricing analyst at an insurer. Management suspects some customers pay far less than they cost while others pay far more. If that's true, overcharged low-risk customers leave for competitors and undercharged high-risk customers stay, so the portfolio gets steadily worse. I built a risk-based price for every policy in Python, tested it against a machine-learning challenger, measured how much premium is shifted between customers, and built a five-page Power BI dashboard for pricing managers.

### Key business questions
1. What does the portfolio look like, and how are claims and claim costs distributed?
2. Which customer and vehicle characteristics drive how often customers claim and how much claims cost?
3. What is a fair, risk-based price for each policy?
4. Which customer groups are subsidised or overcharged under the current tariff, and by how much?

### Key insights
- **A few large claims drive the cost.** 95% of policies had no claim, and the largest 1% of claims make up **30.7% of total claim cost**.
- **Vehicle age, no-claims history (bonus-malus) and driver age** are what separate low-risk from high-risk customers. Once a claim happens, its cost is similar for almost everyone.
- **The risk-based price works on unseen customers:** actual claims came within 1.5% of what was expected, and actual cost rises **6.4× from the safest to the riskiest 10%** of customers.
- **The current tariff shifts EUR 15.0M a year (17.7% of premium) between customers.** Owners of new vehicles pay only 0.29 of their expected cost, while the safest drivers pay 1.10 times theirs.
- **Under the current tariff, the riskiest 10% of customers cost twice what they pay** (loss ratio 2.01) while the safest 10% pay more than double what they cost (0.47). Under the risk-based price, every group stays between 0.93 and 1.05.
- **The business risk is real:** if overcharged customers left for a competitor with risk-based pricing, the remaining customers would need a **29.4% price rise** to break even.

**Recommendation:** move to risk-based pricing, phase in large increases to limit customer backlash, price new vehicles properly, and keep the machine-learning model as an ongoing check on what the tariff misses.

---

## 2. HR Analytics: Workforce, Turnover and Attrition Risk

![Risk tiers: share of employees vs share of expected attrition cost](https://raw.githubusercontent.com/celynhs/HR-Analytics/main/images/hr_risk_tier_cost.png)

**Tech stack:** SQL (Google BigQuery) · Python (pandas, NumPy, SciPy, statsmodels, scikit-learn, Matplotlib, Seaborn)

**Repository:** [github.com/celynhs/HR-Analytics](https://github.com/celynhs/HR-Analytics)

### What the project is about
An end-to-end HR analysis in two parts, each on its own dataset. **Part A (SQL)** covers workforce and turnover reporting for a 311-employee company: headcount, turnover trends, exit reasons, hiring channels, manager effects and pay equity. **Part B (Python)** uses 5,000 employee records to find what drives attrition, build a model that flags at-risk employees, and estimate what targeted retention would save.

### Key business questions
1. Is turnover rising or falling, and where is it concentrated?
2. Why do people leave, and how many exits could have been prevented?
3. Which hiring channels bring people who stay?
4. Are we losing strong performers, and is pay fair between men and women?
5. What drives attrition, can we spot at-risk employees early, and what would acting on it save?

### Key insights
- **Turnover is concentrated in Production**, which loses people at 2.7× the rate of Sales and accounts for 80% of exits.
- **Half of all exits could have been prevented:** 51% were for pay, hours, unhappiness or a better offer.
- **The company is losing its best people.** 77% of exits were strong performers who chose to leave, and engagement scores did not flag them in advance.
- **Referrals and LinkedIn bring the employees who stay** (93% and 90% still employed after 3 years), while Google Search is the weakest channel (71%).
- **There is no like-for-like gender pay gap.** The overall 1.5–2.0% gap comes from more women working in lower-paid Production roles, not from unequal pay for the same job.
- **Burnout, poor manager support and stalled promotions drive attrition** far more than pay level or demographics.
- **Attrition costs about $35.5M a year.** The risk model finds 45.5% of future leavers in the riskiest 20% of employees, and a targeted retention package for the highest-risk group could save about **$6.54M a year**.

**Recommendation:** retain experienced Production staff, track regretted attrition as its own KPI, shift hiring budget to referrals and LinkedIn, invest in reducing burnout and in manager quality, and use the risk model to focus retention spending.

---

## 3. E-commerce Sales Analysis

![Monthly realized revenue](https://raw.githubusercontent.com/celynhs/Sales-Analysis/main/images/monthly_realized_revenue.png)

**Tech stack:** Python (pandas, NumPy, SciPy, Matplotlib)

**Repository:** [github.com/celynhs/Sales-Analysis](https://github.com/celynhs/Sales-Analysis)

### What the project is about
An analysis of 50,000 orders from an online electronics retailer (January 2024 – June 2026), using four linked tables of orders, payments, customers and products. I cleaned and reconciled the data, then analysed revenue performance, product mix, revenue lost to cancellations, returns and payment problems, customer value and whether discounts work.

### Key business questions
1. How has revenue changed month by month, and is there a seasonal pattern?
2. Which categories and products bring in the most revenue and the most orders?
3. How much potential revenue is lost, and where does it come from?
4. Who are our most valuable customers, and who should the business focus on?
5. Do discounts make customers buy more?

### Key insights
- **Revenue was flat at about 105K a month, then dropped about 32% from February 2026** across every segment at once, which points to a technical or channel problem rather than changing customer behaviour.
- **Electronics brings in 51% of revenue**, and half the product range brings in 71%. Cheap accessories drive order volume, not revenue.
- **14.4% of potential revenue (504K) is lost**, mostly because order and payment records don't match, not because sales are lost. This includes 3,711 orders where a refund may be owed and unpaid orders that were still delivered.
- **Customer labels, age and city don't predict customer value; buying behaviour does.** 22% of buyers bring in 32% of revenue, and 1,666 previously valuable customers have gone quiet.
- **65% of orders are discounted, costing 246K, but discounts don't make customers buy more.**

**Recommendation:** verify the February 2026 drop with the data team, fix order–payment reconciliation, win back high-value customers who have gone quiet, and cut blanket discounting (testing any targeted discount first).

---

## Contact

I'm open to data analyst roles, including remote positions. Feel free to reach out:

📧 celinhelsa28@gmail.com · 💼 [LinkedIn](https://www.linkedin.com/in/jocelin-helsa-418092264)
