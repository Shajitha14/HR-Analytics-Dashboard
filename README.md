HR Analytics Dashboard — Employee Attrition Analysis
<img width="1366" height="768" alt="Screenshot 2026-06-12 192722" src="https://github.com/user-attachments/assets/7126eae3-dadb-4f7f-9b44-2a0c5bfbde7f" />
<img width="1366" height="768" alt="Screenshot 2026-06-12 192746" src="https://github.com/user-attachments/assets/a3c2a4bf-df61-4dee-824d-36826886d401" />
<img width="1366" height="768" alt="Screenshot 2026-06-12 192802" src="https://github.com/user-attachments/assets/c65049c2-b06c-4c05-848b-60ea96e348ca" />
Employee attrition is one of the most costly challenges organisations face. This project dives into the IBM HR Analytics dataset to uncover who is leaving, why they might be leaving, and where the organisation should focus its retention efforts.

The dashboard is designed for HR managers and business leaders who need clear, actionable insights  not just raw numbers.
🎯 Business Questions Answered


1.What is the overall attrition rate across the organisation?
2.Which departments have the highest attrition?
3.Does salary slab impact employee retention?
4.Which age groups are most likely to leave?
5.How does overtime affect attrition?
6.Which job roles and job levels see the most exits?
6.Do employees leave more in their early years at the company?
📁 Dataset

Detail   -  Info
Source      IBM HR Analytics Attrition Dataset — Kaggle
Records     1,470 employees
Features    35 columns
Target      variableAttrition (Yes / No)

 Tools & Technologies

Tool        Purpose
Power       BI  DesktopDashboard design and visualisation
Power       Query (M)Data cleaning and transformation
DAX         Custom measures and KPI calculations
Excel / CSV Raw data source

-- Attrition Rate
Attrition Rate = 
DIVIDE(
    CALCULATE(COUNT(HR_Analytics[Attrition]), HR_Analytics[Attrition] = "Yes"),
    COUNT(HR_Analytics[Attrition]),
    0
)

-- Total Attrition Count
Total Attrition = 
CALCULATE(COUNT(HR_Analytics[Attrition]), HR_Analytics[Attrition] = "Yes")

-- Active Employees
Active Employees = 
CALCULATE(COUNT(HR_Analytics[Attrition]), HR_Analytics[Attrition] = "No")

-- Average Age
Avg Age = AVERAGE(HR_Analytics[Age])

Dashboard Features

KPI Cards


✅ Total Employees
✅ Total Attrition Count
✅ Attrition Rate %
✅ Average Age of Employees
