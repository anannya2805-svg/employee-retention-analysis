# Employee Retention & Workforce Productivity Analysis
**Tool:** Microsoft Excel

## The Problem
The company is losing more employees than expected, and replacing them is expensive (roughly 6–9 months of salary per employee, based on industry estimates). HR didn't have clear data on *why* people were leaving — was it pay, overtime, lack of training, or something specific to certain departments?

## What I Set Out to Answer
1. Which department has the most people leaving, and by how much?
2. Does working overtime make people less satisfied and more likely to quit?
3. Does completing training actually improve performance?
4. Does pay level affect who leaves?

## What I Did
- **Cleaned the data:** The raw file had inconsistent spelling, extra spaces, missing department names, and duplicate rows. I used TRIM, CLEAN, and XLOOKUP to fix and fill in this data.
- **Built Pivot Tables:** To compare attrition, satisfaction, and performance across departments, overtime levels, training status, and pay brackets.
- **Ran simple statistical checks:** Used correlation and a t-test to confirm whether the patterns I saw were real, not just random chance.
- **Built a Dashboard:** Combined the findings into charts with clickable filters (slicers) so anyone can explore the data by department or training status.

## What I Found

**Sales has the highest attrition (about 41%)** — much higher than any other department, including Human Resources (about 14%).

**Overtime has the biggest impact on satisfaction.** I checked this using correlation, a simple way of measuring whether two things tend to rise or fall together. The result showed a moderate negative relationship — in plain terms, the more overtime someone works, the less satisfied they tend to be, fairly consistently. This turned out to be the strongest relationship in the whole dataset. It doesn't rise gradually either — once someone crosses 15 hours of overtime a week, their chance of leaving jumps sharply (from about 11% to 51%).

**Training genuinely helps performance, and this isn't just a coincidence.** Employees who completed training scored noticeably higher (3.37 vs 2.79 out of 4). To make sure this gap was real and not just random luck in who ended up in each group, I ran a statistical significance test (a t-test). It confirmed the difference is highly unlikely to be due to chance — training is genuinely linked to better performance.

**Pay level alone doesn't clearly predict who leaves.** I expected income to matter more, but the correlation between income and attrition came out essentially at zero. This was a useful finding on its own — it suggests workload (overtime) plays a bigger role in retention than pay does.

**Pay is inconsistent within performance groups, not just low.** Looking at how spread out people's salaries were (standard deviation — a measure of how much values vary from the average) within each performance rating group, pay varies a lot within every group, not just that top performers earn more. This suggests salary isn't cleanly tied to how well someone performs — worth investigating separately as a possible fairness or retention concern.

## My Recommendations
1. **Limit weekly overtime**, especially past 15 hours — this is where attrition risk rises the most, and where satisfaction drops off most sharply.
2. **Encourage more employees to complete training** — it's clearly and reliably linked to better performance.
3. **Look closely at what's happening in Sales** specifically, since their attrition is far higher than every other department.

## A Note on the Data
This analysis shows patterns and relationships in the data, not proof of what's directly causing people to leave. A deeper study would be needed to confirm cause and effect.

## Files in This Repo
- `Employee_Retention_Analysis.xlsx` — the full workbook (cleaned data, statistical analysis, dashboard)
- `Rawdataset/` — the raw data of employees
