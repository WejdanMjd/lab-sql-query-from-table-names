# GPT Query Analysis Report

## Summary of Findings

In this experiment, I tested three different prompts to evaluate how well GPT-3.5-turbo can generate structured data insights. The prompts covered employee performance, product sales analysis, and regional market trends. The results were insightful, but there were a few inconsistencies that warrant further analysis.

## Findings per Prompt

### 1. Employee Order Count Prompt
- The response correctly identified that a SQL query is needed to count the total number of orders per employee.
- However, GPT sometimes generated an SQL query without knowing the actual database schema, which could lead to inaccuracies.

### 2. Top 5 Best-Selling Products Prompt
- GPT provided a structured approach to retrieve and calculate the top 5 best-selling products.
- One limitation was that it assumed the existence of certain columns like `total_sales` and `revenue_percentage`, which may not exist in every dataset.

### 3. Regional Market Trends Heatmap Prompt
- GPT attempted to describe how to create a heatmap but did not generate actual code for visualization.
- It suggested using Python libraries such as Matplotlib and Seaborn but did not consider the need for properly formatted regional data.
- The response lacked specificity in terms of actionable insights for marketing efforts.

## Issues Encountered

### Hallucinations
- In some cases, GPT fabricated column names and database structures that may not exist in a real-world dataset.

### Overgeneralization
- Some responses were too generic and required additional refinement to be applicable in a practical setting.

### Lack of Context Awareness
- GPT struggled with dynamically adjusting its response based on missing information, often making assumptions about table structures and available data.

## Lessons Learned

### Prompt Engineering is Key
- The way a question is phrased significantly impacts the response quality. More specific and structured prompts yield better results.

### GPT is Not a Database Expert
- While GPT can generate SQL queries and suggest analytical approaches, it lacks real-time access to actual databases and must rely on user-provided schemas.

### Post-Processing is Necessary
- Responses often need human validation and refinement before implementation, especially when dealing with real-world business data.

## Recommendations for Future Use
- Use structured data schemas as input to improve GPT’s accuracy.
- Validate AI-generated queries before running them on production databases.
- Experiment with few-shot prompting to guide GPT toward more reliable responses.

By refining prompt design and verifying outputs, GPT can serve as a valuable tool for business intelligence and data analytics, but human oversight remains essential.
