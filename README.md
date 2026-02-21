# Snowflake Cortex Code (CoCo) Tutorial

- Cortex Code provides an agentic experience across several functional areas within Snowsight.
- It is designed to assist data analysts, engineers, and administrators with tasks such as SQL development, data exploration, and account management by deeply integrating into the Snowsight interface and offering capabilities such as diff views.
- Cortex Code uses intelligent orchestration to plan and execute multi-step tasks based on your request.
- In addition, it selects internal tools and relevant context from your Snowflake environment to complete the task, ensuring that each response is accurate.
- Cortex Code understands roles, privileges, schemas, and SQL syntax, and applies Snowflake best practices when it is generating or modifying code. (this is great for single enviornment development)
- Cortex Code in Snowsight acts as an intelligent agent, helping you work more efficiently by translating natural language instructions into executable actions

## Cortex Code supports the following key functional areas within Snowsight:
Agentic coding in Workspaces

- Code generation and development: Generate SQL queries, create new files, and construct logic for data pipelines and analytics workflows.
- Code modification and optimization: Refine SQL directly in a workspace, identify logic or syntax errors, and suggest optimizations for performance, readability, or cost.
- Change review: Preview AI-suggested changes using a diff view before applying them. The diff view highlights insertions and deletions, allowing users to maintain control over their code.
- Code explanation: Request an explanation of existing SQL to assist with understanding or collaboration.
- Ask follow-up questions: Continue the conversation by asking clarifying questions or requesting further analysis on generated code or results.
- Quick actions from highlighted SQL: In a SQL file, highlight text to open quick actions such as Quick Edit, Format, Add to Chat, and Explain.
- Fix SQL errors: If a SQL statement fails, use the Fix button in the results grid to get suggested fixes for the error.

## Intelligent product and documentation discovery (Not Covering)
Cortex Code uses context from the Horizon Catalog and Snowflake documentation to help you locate data assets and reference information without leaving your workspace

- Natural language schema search: Locate database objects such as tables and columns using plain language queries, without needing to know exact object names.
- Integrated Q & A: Retrieve answers about Snowflake features, SQL syntax, or best practices based on official documentation.
- Snowflake Marketplace discovery:
  
## Role Requirement
- SNOWFLAKE.COPILOT_USER
- SNOWFLAKE.CORTEX_USER
- SNOWFLAKE.CORTEX_AGENT_USER (SNOWFLAKE.CORTEX_AGENT_USER provides additional capabilities for agentic workflows.)

We can use this as last chapter to explain the purpose of role and we must tell user to use the free trial edition.

## Example prompts

### Access and permissions
- What databases do I have access to?
- Find all tables that have PII in them

### Data discovery
- List every table tagged PII = TRUE in ANALYTICS_DB
- Show the lineage from RAW_DB.ORDERS to downstream dashboards
- Where can I find tables related to customer churn and subscription status?

### SQL development and optimization
- What does this SQL script do?
- Write a query for top 10 customers by revenue and a 7-day moving average
- Update the top performers query to show the top 100
- Explain why this query is slow and optimize it
- Generate synthetic data for 30 days of sales for an e-commerce site in the SAMPLESDATA.SALES table

### Infrastructure and cost management
- Which 5 service types are using the most credits? Show me a visualization and how to reduce costs

### Semantic model integration
- Use the @models/revenue.yaml semantic model to answer "What was revenue last month?


## Limitations
- If your account previously opted out of (or disabled) Snowflake Copilot (legacy), Cortex Code will also be disabled.
- Chat history is not maintained in WebUI, but it remembers everything.
- Pricing :Cortex Code in Snowsight is currently free of charge to use. Details on pricing and billing are planned but you will be notified before any charges are applied for this feature. When it becomes chargable, how it is charged is a question.
- Cortex Code in CLI is billed based on token consumption

## To Covered in future

### Web search
AI/ML > Agents.
Settings


## Very Important & Future
- https://agents.md/
- https://agentskills.io/home
