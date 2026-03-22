
> **Theme:** Master the art of making data visual and self-explanatory — build dashboards that tell the story without needing you in the room. Add Tableau to your toolkit and develop forecasting intuition. **Tools:** Power BI Desktop + Tableau Public + Python (Jupyter) + DB Browser for SQLite

---

### Day 1

#### Session 1 — Technical (60 min)

- [ ] Open Tableau Public (download from public.tableau.com if not yet installed)
- [ ] Connect to your cafe CSV file from Month 1
- [ ] Explore the interface: Dimensions vs Measures, Rows/Columns shelves, Marks card
- [ ] Create your first Tableau view: a simple bar chart of sales per product

#### Session 2 — Analytical/Business (60 min)

- [ ] Review Month 4 highlights — re-read `Business-Concepts.md` (Metric Trees, RFM, Visualization Best Practices)
- [ ] Learn the concept: **linear regression intuition** for BI (no heavy math)
    - [ ] What is a trend line and what does it tell you?
    - [ ] Slope = rate of change; intercept = starting point
    - [ ] R² value: how well does the line fit the data? (0 = no fit, 1 = perfect fit)
- [ ] Save in `Statistics-for-BI.md` under "Regression Basics"

---

### Day 2

#### Session 1 — Technical (60 min)

- [ ] Tableau: learn the core building blocks
    - [ ] Drag a date field to Columns → Tableau auto-creates a time axis
    - [ ] Drag a measure to Rows → creates a bar or line chart
    - [ ] Change chart type using the "Show Me" panel on the right
    - [ ] Practice: create a line chart of monthly revenue
- [ ] Note: how does the Tableau drag-and-drop feel compared to Power BI?

#### Session 2 — Analytical/Business (60 min)

- [ ] Add a **trend line** to your Python scatter plot from Month 4
    - [ ] `from scipy.stats import linregress`
    - [ ] `slope, intercept, r_value, p_value, std_err = linregress(x, y)`
    - [ ] Plot the trend line on top of the scatter plot using matplotlib
    - [ ] Interpret: what does the slope and R² tell you about the relationship?
- [ ] Save code + interpretation in your Python notebook

---

### Day 3

#### Session 1 — Technical (60 min)

- [ ] Tableau: learn **filters and quick filters**
    - [ ] Drag a dimension to the Filters shelf
    - [ ] Show the filter as a dropdown on the view
    - [ ] Learn: discrete vs continuous filters
- [ ] Practice: add a category filter and a date range filter to your monthly revenue chart

#### Session 2 — Analytical/Business (60 min)

- [ ] Python: **simple linear regression with scikit-learn**
    - [ ] `pip install scikit-learn` (if not installed)
    - [ ] `from sklearn.linear_model import LinearRegression`
    - [ ] Fit a model: predict next month's revenue based on month number
    - [ ] Interpret: what does the model predict for the next 3 months?
- [ ] Save the model code in a new notebook: `month5-regression.ipynb`

---

### Day 4

#### Session 1 — Technical (60 min)

- [ ] Tableau: learn **calculated fields** — Tableau's equivalent of DAX measures
    - [ ] Right-click in the data pane → Create Calculated Field
    - [ ] Create: `Revenue = quantity * unit_price`
    - [ ] Create: `Profit Margin = (revenue - cost) / revenue`
    - [ ] Add both to your views
- [ ] Note: compare calculated fields in Tableau vs measures in Power BI

#### Session 2 — Analytical/Business (60 min)

- [ ] Learn the concept: **forecasting basics** for BI
    - [ ] What is a forecast and what makes a good one?
    - [ ] Simple approaches: moving average forecast, linear trend extrapolation
    - [ ] Where forecasts break down: seasonality, external shocks, insufficient data
- [ ] Think: what would a 3-month revenue forecast look like for your cafe dataset?
- [ ] Save in `Statistics-for-BI.md` under "Forecasting Concepts"

---

### Day 5

#### Session 1 — Technical (60 min)

- [ ] Tableau: **build your first dashboard**
    - [ ] Create 3 separate sheets: revenue trend, product bar chart, category pie chart
    - [ ] Go to Dashboard tab → New Dashboard
    - [ ] Drag all 3 sheets onto the dashboard canvas
    - [ ] Resize and arrange them cleanly
- [ ] Save your Tableau workbook: `cafe-tableau-v1.twbx`

#### Session 2 — Analytical/Business (60 min)

- [ ] Python: **time series forecasting with moving average**
    - [ ] Create a 30-day moving average forecast: extend the rolling mean into future dates
    - [ ] Plot: actual revenue + moving average + 30-day forecast
    - [ ] Add a shaded confidence region (±1 standard deviation)
- [ ] Interpret: is the forecast useful or does it miss important patterns?

---

### Day 6

#### Session 1 — Technical (60 min)

- [ ] Tableau: **interactivity — using one sheet as a filter for others**
    - [ ] Select a sheet on your dashboard → Use as Filter (funnel icon)
    - [ ] Click a bar → the other charts filter to that category automatically
    - [ ] This is one of Tableau's most powerful features — practice it well
- [ ] Test: click through different products and categories on your dashboard

#### Session 2 — Analytical/Business (60 min)

- [ ] **Weekly Reflection — Week 1 of Month 5:**
    - [ ] Tableau: first impressions vs Power BI — what is each better at?
    - [ ] Regression: does the concept feel usable in real BI work?
    - [ ] What is the most important thing to build this month?
- [ ] Update `Statistics-for-BI.md` and `Business-Concepts.md` with new notes

---

### Day 7

#### Session 1 — Technical (60 min)

- [ ] Tableau: **LOD (Level of Detail) expressions** — Tableau's most powerful feature
    - [ ] Three types: FIXED, INCLUDE, EXCLUDE
    - [ ] `FIXED`: compute at a specified level regardless of view filters
    - [ ] Example: `{ FIXED [Product] : SUM([Revenue]) }` — total revenue per product, always
    - [ ] Practice: show each product's revenue as % of its category total using LOD

#### Session 2 — Analytical/Business (60 min)

- [ ] Power BI: learn **advanced report design — the Z-pattern and F-pattern**
    - [ ] Z-pattern: eye moves top-left → top-right → bottom-left → bottom-right
    - [ ] F-pattern: eye reads left-to-right at the top, then scans down the left side
    - [ ] Place your most important KPIs and visuals in the eye's natural path
- [ ] Redesign your `Project-02-Dashboard-Final.pbix` layout using the Z-pattern
- [ ] Save as `Project-02-Dashboard-v2.pbix`

---

### Day 8

#### Session 1 — Technical (60 min)

- [ ] Tableau: **table calculations** — computed across the view (not the data source)
    - [ ] Right-click a measure pill → Add Table Calculation
    - [ ] Try: Running Total, Percent of Total, Percent Difference from Previous
    - [ ] Practice: show monthly revenue as % of the full year total

#### Session 2 — Analytical/Business (60 min)

- [ ] Power BI: learn **themes and report templates**
    - [ ] File → Options → Report Settings → Customize current theme
    - [ ] Define: primary color, secondary color, font family, background color
    - [ ] Save the theme as a JSON file: `my-report-theme.json`
    - [ ] Apply the same theme to both Project-01 and Project-02 dashboards for consistency

---

### Day 9

#### Session 1 — Technical (60 min)

- [ ] Tableau: **build an executive KPI summary sheet**
    - [ ] Use BAN (Big Ass Number) style cards: large number + label + trend indicator
    - [ ] Create 4 KPI cards: Total Revenue, Total Orders, AOV, Top Product
    - [ ] Use color coding: green if above target, red if below
- [ ] Add the KPI sheet to your cafe dashboard

#### Session 2 — Analytical/Business (60 min)

- [ ] Learn the concept: **multiple regression intuition**
    - [ ] Simple regression: 1 predictor (month → revenue)
    - [ ] Multiple regression: many predictors (month + temperature + promotions → revenue)
    - [ ] Concept: each predictor has a coefficient showing its individual impact
    - [ ] You don't need to build models — but you need to understand what the output means
- [ ] Save in `Statistics-for-BI.md` under "Multiple Regression Intuition"

---

### Day 10

#### Session 1 — Technical (60 min)

- [ ] Python: **multiple regression with scikit-learn**
    - [ ] Create 2–3 fake predictor columns in your dataset (day of week, is_weekend, month_number)
    - [ ] `from sklearn.linear_model import LinearRegression`
    - [ ] Fit the model with multiple features, check R² score
    - [ ] Print feature coefficients: which predictor has the most impact?
- [ ] Add this to `month5-regression.ipynb` with interpretation notes

#### Session 2 — Analytical/Business (60 min)

- [ ] Learn the concept: **dashboard design patterns**
    - [ ] Overview → Detail → Filter pattern: start broad, allow drilling into specifics
    - [ ] The "newspaper front page" rule: the most important insight should be impossible to miss
    - [ ] White space is not wasted space — it guides the eye
- [ ] Apply 2 of these patterns to your current Tableau dashboard
- [ ] Save in `Business-Concepts.md` under "Dashboard Design Patterns"

---

### Day 11

#### Session 1 — Technical (60 min)

- [ ] Tableau: **parameters** — interactive user inputs (similar to Power BI what-if parameters)
    - [ ] Create a parameter: "Target Revenue" (integer, range 0–1,000,000)
    - [ ] Create a calculated field: `Above Target = SUM([Revenue]) > [Target Revenue]`
    - [ ] Use the parameter to dynamically color-code bars: green if above target, red if below
- [ ] Add a parameter control slider to your dashboard

#### Session 2 — Analytical/Business (60 min)

- [ ] Learn the concept: **cohort retention heatmaps** — a classic BI visualization
    - [ ] Rows: cohort month (when the user first appeared)
    - [ ] Columns: months since first purchase (0, 1, 2, 3...)
    - [ ] Values: % of original cohort still active in that month
    - [ ] Build one in Tableau using your e-commerce data from the SQL cohort query (Month 2)
- [ ] Save the visualization to your Tableau workbook

---

### Day 12

#### Session 1 — Technical (60 min)

- [ ] Power BI: **performance analyzer** — measure how fast your report renders
    - [ ] View tab → Performance Analyzer → Start Recording → Refresh Visuals
    - [ ] Identify which visuals are slowest to render
    - [ ] Optimize: reduce the number of measures evaluated at once, simplify DAX where possible
- [ ] Apply to your Project-02 dashboard — aim for all visuals under 1 second

#### Session 2 — Analytical/Business (60 min)

- [ ] **Weekly Reflection — Week 2 of Month 5:**
    - [ ] Tableau: can you now build an interactive, multi-sheet dashboard from scratch?
    - [ ] Power BI: has your design quality improved since Month 1?
    - [ ] Regression/forecasting: how would you use these in a real BI project?
- [ ] List 3 things you want to build or improve before end of month

---

### Day 13

#### Session 1 — Technical (60 min)

- [ ] Tableau: **dual-axis charts** — plot two measures on the same chart
    - [ ] Drag a second measure to the right side of the view → creates a second axis
    - [ ] Synchronize axes: right-click the second axis → Synchronize Axis
    - [ ] Example: bar chart of revenue + line chart of order count on the same view
- [ ] Add a dual-axis chart to your Tableau dashboard

#### Session 2 — Analytical/Business (60 min)

- [ ] Learn the concept: **AB test analysis for BI Analysts**
    - [ ] You won't design the test — but you'll often be asked to analyze the results
    - [ ] Key questions: Is the difference statistically significant? What is the effect size?
    - [ ] Python practice: simulate an AB test — group A (100 users, 10% conversion), group B (100 users, 13% conversion)
    - [ ] Run a chi-square test: `stats.chi2_contingency([[10,90],[13,87]])`
    - [ ] Interpret the p-value and what it means for the business decision

---

### Day 14

#### Session 1 — Technical (60 min)

- [ ] SQL: **interview preparation — set 3 (visualization-focused queries)**
    - [ ] "Write a query that produces data ready for a cohort retention heatmap"
    - [ ] "Produce a dataset of weekly revenue with WoW % change for a line chart"
    - [ ] "Generate a customer-level RFM table ready to be imported into a BI tool"
    - [ ] "Write a query to produce a funnel table: step name, user count, conversion %"
- [ ] These are real queries BI Analysts write to feed their dashboards

#### Session 2 — Analytical/Business (60 min)

- [ ] **Weekly Reflection — Week 2 into 3 of Month 5:**
    - [ ] SQL: how fast can you write a "dashboard-ready" query from scratch?
    - [ ] What have you learned about how SQL and visualization tools work together?
- [ ] Review all 4 projects so far (Month 1 mini, Month 2 mini, Project-01, Project-02)
- [ ] Write: "What would I do differently if I rebuilt each one today?"

---

### Day 15

#### Session 1 — Technical (60 min)

- [ ] Tableau: **story points** — guided, presentation-ready narratives inside Tableau
    - [ ] Go to Story tab → New Story
    - [ ] Add your dashboard sheets as story points
    - [ ] Add captions to each point: "Revenue is growing..." → "But weekends underperform..." → "Recommendation: ..."
    - [ ] This is Tableau's built-in storytelling feature — great for stakeholder presentations

#### Session 2 — Analytical/Business (60 min)

- [ ] Learn the concept: **the Minto Pyramid Principle** for data communication
    - [ ] Start with the conclusion (the "so what"), then support it with evidence
    - [ ] Most people bury the insight at the end — BI Analysts should lead with it
    - [ ] Example: "We should focus on the East region (conclusion) because it has 40% higher LTV but only 20% of our ad spend (evidence)"
- [ ] Rewrite your `Project-02-Insights.md` using the Pyramid Principle structure
- [ ] Save in `Business-Concepts.md` under "Communication Frameworks"

---

### Day 16

#### Session 1 — Technical (60 min)

- [ ] Python: **seaborn advanced charts for BI**
    - [ ] Heatmap: `sns.heatmap(pivot_table, annot=True, fmt='.0f', cmap='RdYlGn')`
    - [ ] Pair plot: `sns.pairplot(df[['revenue', 'quantity', 'price']])` — see all correlations at once
    - [ ] Box plot with hue: `sns.boxplot(x='category', y='revenue', hue='is_weekend', data=df)`
- [ ] Practice all 3 on your Kaggle dataset and add to your Python notebook

#### Session 2 — Analytical/Business (60 min)

- [ ] Power BI: **decomposition tree visual**
    - [ ] Insert → Decomposition Tree
    - [ ] Set Analyze: Total Revenue; Explain By: Category, Product, Region, Month
    - [ ] Use it to find the biggest drivers of a revenue change
    - [ ] This visual alone can replace hours of SQL drilling in exploratory analysis

---

### Day 17

#### Session 1 — Technical (60 min)

- [ ] Power BI: **key influencers visual**
    - [ ] Insert → Key Influencers
    - [ ] Analyze: what influences a customer to be high-value?
    - [ ] This visual uses machine learning under the hood — no code required
    - [ ] Explore: what factors most increase/decrease the target metric?
- [ ] Add to `Project-02-Dashboard-v2.pbix` as a bonus insights page

#### Session 2 — Analytical/Business (60 min)

- [ ] Learn the concept: **data-driven storytelling structure for presentations**
    - [ ] Hook: open with a surprising or counterintuitive finding
    - [ ] Context: what was the situation before the analysis?
    - [ ] Finding: what does the data show?
    - [ ] Implication: what does this mean for the business?
    - [ ] Recommendation: what should happen next?
- [ ] Apply this 5-part structure to your best finding from Project-02
- [ ] Save in `Business-Concepts.md` under "Presentation Structure"

---

### Day 18

#### Session 1 — Technical (60 min)

- [ ] **End-of-Month Project — Tableau Dashboard:**
    - [ ] Load your Kaggle dataset into Tableau Public
    - [ ] Build a 3-sheet dashboard:
        - [ ] Sheet 1: Revenue KPI cards + time trend (dual-axis: revenue bar + order count line)
        - [ ] Sheet 2: Customer segments (cohort retention heatmap or RFM scatter)
        - [ ] Sheet 3: Product performance (sorted bar chart + category filter)
    - [ ] Apply all visualization best practices from this month

#### Session 2 — Analytical/Business (60 min)

- [ ] Add interactivity to the Tableau dashboard:
    - [ ] Use Sheet 1 as a filter for Sheets 2 and 3
    - [ ] Add a parameter: Target Revenue with conditional coloring
    - [ ] Add a date range filter as a quick filter on the dashboard
- [ ] Save as `Project-03-Tableau.twbx`

---

### Day 19

#### Session 1 — Technical (60 min)

- [ ] **End-of-Month Project — Story Points:**
    - [ ] Create a Tableau Story from your dashboard
    - [ ] 4–5 story points following the 5-part data storytelling structure:
        - [ ] Point 1: Hook — the most surprising finding
        - [ ] Point 2: Context — what the data looks like overall
        - [ ] Point 3: Finding — the key insight
        - [ ] Point 4: Implication — what it means
        - [ ] Point 5: Recommendation — what to do next
    - [ ] Write clear captions for each story point

#### Session 2 — Analytical/Business (60 min)

- [ ] **Weekly Reflection — Week 3 of Month 5:**
    - [ ] Tableau: can you now build a complete, interactive, narrative dashboard?
    - [ ] Storytelling: does your Pyramid Principle + 5-part structure feel natural yet?
    - [ ] Which tool — Power BI or Tableau — do you currently feel stronger in?
- [ ] Update all notes and cheatsheets

---

### Day 20

#### Session 1 — Technical (60 min)

- [ ] Python: **forecasting with Prophet** (Facebook's open-source forecasting library)
    - [ ] `pip install prophet`
    - [ ] `from prophet import Prophet`
    - [ ] Format your data: columns must be named `ds` (date) and `y` (value)
    - [ ] Fit the model: `m = Prophet(); m.fit(df)`
    - [ ] Forecast 90 days: `future = m.make_future_dataframe(periods=90); forecast = m.predict(future)`
    - [ ] Plot: `m.plot(forecast)`

#### Session 2 — Analytical/Business (60 min)

- [ ] Interpret the Prophet forecast:
    - [ ] What is the trend component showing?
    - [ ] Is there a weekly or yearly seasonality pattern?
    - [ ] How wide are the confidence intervals — how certain is the forecast?
- [ ] Write a 1-paragraph forecast narrative for your Kaggle dataset
- [ ] Save code + narrative in `month5-regression.ipynb`

---

### Day 21

#### Session 1 — Technical (60 min)

- [ ] Power BI: **publish to Power BI Service** (cloud)
    - [ ] Sign in with a free Microsoft account at app.powerbi.com
    - [ ] From Power BI Desktop: File → Publish → My Workspace
    - [ ] Open the published report in a browser
    - [ ] Explore: how does the report look and behave in the cloud vs desktop?
- [ ] Note: Power BI Service is what end users typically see in a real company

#### Session 2 — Analytical/Business (60 min)

- [ ] Learn the concept: **self-service BI** — empowering non-technical users to explore data themselves
    - [ ] What is self-service BI and why do companies invest in it?
    - [ ] Tools: Power BI, Tableau, Looker, Metabase — each has a different philosophy
    - [ ] Trade-offs: flexibility vs governance, speed vs accuracy
- [ ] Save in `Business-Concepts.md` under "BI Strategy & Culture"

---

### Day 22

#### Session 1 — Technical (60 min)

- [ ] Build **Month 5 Tableau cheatsheet** in a new file: `Tableau-Basics.md`
    - [ ] Core interface: Dimensions vs Measures, Rows/Columns, Marks card
    - [ ] Chart types + when to use each
    - [ ] Filters: discrete vs continuous, quick filters
    - [ ] Calculated fields: syntax and examples
    - [ ] LOD expressions: FIXED, INCLUDE, EXCLUDE with examples
    - [ ] Table calculations: running total, % of total, % difference
    - [ ] Parameters: how to create and use them
    - [ ] Dashboard interactivity: use as filter, actions
    - [ ] Story points: structure and captions
- [ ] Save in `Belajar/03. BI Analyst/`

#### Session 2 — Analytical/Business (60 min)

- [ ] Build **Month 5 Statistics additions** to `Statistics-for-BI.md`:
    - [ ] Linear regression: slope, intercept, R² interpretation
    - [ ] Multiple regression: coefficients and feature importance
    - [ ] Forecasting approaches: moving average, linear trend, Prophet
    - [ ] AB test analysis: chi-square test, p-value interpretation
    - [ ] Cohort retention: how to build and read a retention heatmap

---

### Day 23

#### Session 1 — Technical (60 min)

- [ ] SQL: **interview preparation — set 4 (analytics-heavy)**
    - [ ] "Write a query to calculate rolling 7-day retention rate"
    - [ ] "Find the first and last purchase date for every customer, and the days between them"
    - [ ] "Identify customers who placed exactly 2 orders and never returned"
    - [ ] "Calculate the percentage of revenue contributed by the top 10% of customers"
- [ ] Time yourself — aim for under 12 minutes per query

#### Session 2 — Analytical/Business (60 min)

- [ ] Practice the **Pyramid Principle** with 3 different findings from your projects:
    - [ ] Write each as: Conclusion (1 sentence) → Evidence (2–3 bullets) → So What (1 sentence)
    - [ ] Read them aloud — do they flow naturally?
    - [ ] Ask yourself: "Would a busy manager understand this in 30 seconds?"
- [ ] Save the best example in `Business-Concepts.md` as a template

---

### Day 24

#### Session 1 — Technical (60 min)

- [ ] Tableau Public: **publish your dashboard online**
    - [ ] Server → Tableau Public → Save to Tableau Public
    - [ ] Your dashboard is now live at public.tableau.com/profile/[your-username]
    - [ ] Copy the public link — this is a direct portfolio URL you can share with recruiters
- [ ] Polish before publishing: check all labels, titles, and captions one final time

#### Session 2 — Analytical/Business (60 min)

- [ ] Create a **portfolio entry** for Project-03:
    - [ ] Write a 3-paragraph description:
        - [ ] Paragraph 1: What dataset, what business questions
        - [ ] Paragraph 2: What you did (tools, techniques, analysis)
        - [ ] Paragraph 3: What you found and recommended
    - [ ] Save as `Project-03-Portfolio-Write-Up.md` in the project folder
    - [ ] This write-up can go directly on a portfolio website, LinkedIn, or CV

---

### Day 25

#### Session 1 — Technical (60 min)

- [ ] **Tableau vs Power BI comparison exercise:**
    - [ ] Recreate the same chart in both tools: a dual-axis monthly revenue + order count chart
    - [ ] Compare: which was faster to build? Which looks better? Which is more flexible?
    - [ ] Write your honest assessment in `Tableau-Basics.md` under "Tableau vs Power BI"
- [ ] This is a common interview question — have a clear, nuanced answer ready

#### Session 2 — Analytical/Business (60 min)

- [ ] Learn the concept: **what BI Analysts actually do day-to-day** at different company sizes
    - [ ] Startup: wear many hats — SQL, dashboards, ad-hoc analysis, sometimes data engineering
    - [ ] Mid-size: more specialized — own dashboards, run analyses, present to stakeholders
    - [ ] Enterprise: highly specialized — strict processes, governance, large team
- [ ] Reflect: which environment sounds most appealing to you and why?
- [ ] Save in `Business-Concepts.md` under "BI Career Landscape"

---

### Day 26

#### Session 1 — Technical (60 min)

- [ ] Python: **export analysis results to a formatted Excel report**
    - [ ] Use `openpyxl` (install if needed): `pip install openpyxl`
    - [ ] Write a script that: loads data → runs groupby analysis → exports to Excel with:
        - [ ] Multiple sheets (one per analysis section)
        - [ ] Bold headers, auto-column width
        - [ ] Colored header row
    - [ ] Save as `formatted_report_export.py`

#### Session 2 — Analytical/Business (60 min)

- [ ] **Month 5 comprehensive review:**
    - [ ] Tableau: can you build a publish-ready, interactive dashboard end-to-end?
    - [ ] Power BI: has your design quality and DAX confidence improved since Month 4?
    - [ ] Forecasting: can you run and interpret a Prophet forecast?
    - [ ] Storytelling: do your insights follow the Pyramid Principle?
- [ ] Update skills inventory in `Business-Concepts.md`

---

### Day 27

#### Session 1 — Technical (60 min)

- [ ] SQL: **final interview prep for Intermediate phase — mixed set**
    - [ ] "Write a query to produce a weekly cohort retention table"
    - [ ] "Find products that appear in the top 3 for at least 3 different months"
    - [ ] "Calculate the average time between consecutive orders per customer"
    - [ ] "Show the month with the highest and lowest revenue per product category"
- [ ] Review all 16 interview queries from Months 4–5 — which categories are weakest?

#### Session 2 — Analytical/Business (60 min)

- [ ] Learn the concept: **common BI Analyst interview question types**
    - [ ] SQL coding challenges (you've been practicing these)
    - [ ] Case studies: "Revenue dropped 20% — how would you investigate?"
    - [ ] Behavioral: "Tell me about a time you used data to change a business decision"
    - [ ] Tool-specific: "Walk me through how you'd build this dashboard"
- [ ] Write a prepared answer for the "Revenue dropped 20%" case study using your metric tree framework
- [ ] Save in `Business-Concepts.md` under "Interview Preparation"

---

### Day 28

#### Session 1 — Technical (60 min)

- [ ] Organize all Month 5 files:
    - [ ] Tableau workbooks → `Belajar/03. BI Analyst/05. Projects/Project-03/`
    - [ ] Python regression notebook → same folder
    - [ ] Cheatsheets: `Tableau-Basics.md` → `Belajar/03. BI Analyst/`
    - [ ] Portfolio write-up → project folder
- [ ] Make sure `Tableau-Basics.md` and all cheatsheets are complete and well-organized

#### Session 2 — Analytical/Business (60 min)

- [ ] Write your **Month 5 progress summary**:
    - [ ] New tool mastered: Tableau
    - [ ] New statistical skills: regression, forecasting, AB test analysis
    - [ ] New communication skill: Pyramid Principle, data storytelling structure
    - [ ] Dashboards published: Power BI Service + Tableau Public (live URLs)
- [ ] These live URLs are portfolio assets — save them somewhere accessible

---

### Day 29

#### Session 1 — Technical (60 min)

- [ ] **"Real-world simulation" — Level 5:**
    - [ ] Scenario: a VP asks for a forecast of next quarter's revenue and the key risks
    - [ ] Build: a Prophet forecast on your Kaggle dataset for the next 90 days
    - [ ] Layer on: a Tableau viz showing forecast + confidence interval + historical trend
    - [ ] Write: a 1-page "forecast brief" with the Pyramid Principle structure

#### Session 2 — Analytical/Business (60 min)

- [ ] Preview Month 6 — read ahead on:
    - [ ] What is dbt (data build tool) and why it matters for BI?
    - [ ] What is Google Looker Studio (free, browser-based BI tool)?
    - [ ] Advanced SQL: window frames, recursive CTEs in practice
- [ ] Write 3 specific learning goals for Month 6

---

### Day 30

#### Session 1 — Technical (60 min)

- [ ] **Final technical review — Month 5:**
    - [ ] Tableau: build a 2-sheet interactive dashboard from scratch in under 30 minutes
    - [ ] Python: run a Prophet forecast and plot it — from memory, no looking at notes
    - [ ] Power BI: apply the Z-pattern layout and Pyramid Principle insights to a new 1-page report
- [ ] Note what you couldn't do and add to your "still need to practice" list

#### Session 2 — Analytical/Business (60 min)

- [ ] **Final reflection — Month 5:**
    - [ ] You are now 5 months in and halfway through the roadmap
    - [ ] Write an honest mid-point self-assessment:
        - [ ] What are your 3 strongest skills right now?
        - [ ] What are your 3 biggest gaps?
        - [ ] What would a job description for "Junior BI Analyst" ask for — and how much of it can you do?
    - [ ] This assessment will guide how you prioritize Months 6–12

---

## 🎯 Month 5 End Goals

- [ ] Can build and publish an interactive Tableau dashboard end-to-end (including to Tableau Public)
- [ ] Know core Tableau features: LOD expressions, table calculations, parameters, story points, dashboard actions
- [ ] Can run and interpret a linear regression, multiple regression, and Prophet time series forecast in Python
- [ ] Can analyze an AB test result using a chi-square test and interpret p-values
- [ ] Apply the Minto Pyramid Principle and 5-part storytelling structure to BI findings
- [ ] Published at least 1 dashboard to both Power BI Service and Tableau Public (live portfolio URLs)
- [ ] Completed Project-03 with Tableau dashboard + story + portfolio write-up
- [ ] Can write a prepared, structured answer to the "Revenue dropped 20%" interview case study

---

> 🔭 **Month 6 Preview:** The final Intermediate month — you'll close the phase with advanced SQL patterns (window frames, complex recursive CTEs), an intro to dbt concepts and modern data stack thinking, Google Looker Studio, and a comprehensive Intermediate phase capstone project that ties together everything from Months 4–6.