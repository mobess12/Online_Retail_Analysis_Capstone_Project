# **Online Retail Analysis - Capstone Project**

Online Retail Analysis is a data driven tool designed to support business decision making through comprehensive analysis and visualisation. Built with Python and key libraries including Pandas, Plotly, Seaborn, Matplotlib, SKLearn, Tableau, the tool ingests raw CSV data, processes it efficiently, and delivers actionable insights via interactive visualisations in both Jupyter Notebook and Tableau.

# ![CI logo](https://codeinstitute.s3.amazonaws.com/fullstack/ci_logo_small.png)

## 📘 Table of Contents

1. [Dataset Content](#dataset-content)
2. [Business Requirements](#business-requirements)
3. [Business Goals](#business-goals)
4. [Hypothesis and How to Validate?](#hypothesis-and-how-to-validate)
5. [Project Plan](#project-plan)
6. [Rationale for Visualisations](#rationale-for-visualisations)
7. [Analysis Techniques Used](#analysis-techniques-used)
8. [Ethical Considerations](#ethical-considerations)
9. [Wireframe](#wireframe)
10. [Dashboard Design](#dashboard-design)
11. [KanBan Board](#kanban-board)
12. [Unfixed Bugs](#unfixed-bugs)
13. [Development Roadmap](#development-roadmap)
14. [Deployment](#deployment)
15. [Main Data Analysis Libraries](#main-data-analysis-libraries)
16. [Credits](#credits)
17. [Acknowledgements](#acknowledgements)

## Dataset Content

Online Retail Dataset can be found [here]( https://www.kaggle.com/datasets/abhishekrp1517/online-retail-transactions-dataset)

The online retail dataset contains transactional data of 13 months, including product details, quantities, prices, purchase timestamps, customer IDs, and country information. It can be used to analyse customer behavior, identify popular products, and support pricing and marketing strategies. It's suitable for data analysis and machine learning. 

Column Descriptors:

- StockCode: A code used to identify the product that was purchased
- Description: A brief description of the product that was purchased
- Quantity: The quantity of the product that was purchased
- InvoiceDate: The date and time that the purchase was made
- UnitPrice: The price of one unit of the product that was purchased
- CustomerID: The unique identifier for the customer who made the purchase
- Country: The country where the customer who made the purchase is located


## Business Requirements

**Sales Performance Analysis**

- Analyse sales trends over time to identify peak periods and seasonal patterns for strategic planning.

**Identifying High Value Customers**

- Segment customers to identify high value and high potential groups, enabling targeted marketing and personalised engagement strategies.

**Enhancing Customer Retention**

- Identify repeat customers and analyse their purchase behaviors—such as purchase frequency and average transaction value to improve loyalty programs.

**Product Performance**

- Determine top selling products and product categories, and evaluate inventory turnover to optimise stock management.

**Geographical Insights**

- Examine sales performance by country or region to target marketing efforts and expand in high potential markets.

**Inventory Management**

- Leverage sales data to make informed inventory decisions prioritising products to stock and identifying slow moving items for discontinuation.

## Business Goals

- **Increase Sales Growth**
    - Implement strategies to increase revenue during periods of low customer activity.

- **Targeted and Personalised Marketing**
    - Use customer data to deliver relevant campaigns that drive engagement.

- **Customer Retention & Acquisition**
    - Strengthen loyalty among existing customers while attracting new ones through focused initiatives.

- **Inventory and Supply Chain Optimisation**
    - Enhance efficiency by aligning stock levels and logistics with demand trends.

- **Sustainable Growth**
    - Leverage analytics to inform long term strategic decisions and business development.

- **Regional market expansion**
    - Identify and enter high potential geographic markets to grow brand presence.


## Hypothesis and how to validate?

Hypothesis 1 - Customers in the United Kingdom spend more than those not in the United Kingdom per transaction.

- Using a boxplot is effective because it provides a clear visual comparison of distribution, central tendency, and variability between the two groups.

Hypothesis 2 - Average sales are the same on weekdays and weekends.

- Using a bar chart is effective because it provides a simple and direct visual comparison of group means, which is exactly what the hypothesis is testing. 

Hypothesis 3 - Seasonal spend - Holiday (Black Friday and Christmas) months have a different average transaction value.

- Using a bar chart to is a great choice because it clearly summarizes and compares average transaction values across categories.

To validate the hypothesis, a ttest will be used to obtain the P Value. This will help understand whether they are true or false.

Additionally, validation for these hypotheses will include visualisations and commentary within the data visualisations Jupyter Notebook. Commentary will include, key insights, conclusions, recommendations and improvements, and ethical and societal considerations.

## Project Plan
1. Data Collection
    - Gather the dataset from Kaggle
    - Unzip folder and extract contents to be imported into VSCode
2.  Ethical, Legal and Social Implications
    - Provide the implications and importance of each element.
3. Data Cleaning and Preprocessing
    - Investigate dataset on Microsoft Excel
    - Handle null values, remove duplicates, and correct data types to appropriate ones 
    - Remove irrelevant data (e.g., transactions with negative quantities, product descriptions that are not products such as "damages and ?")
    - Create new features Total Transaction Value (Quantity*UnitPrice)
    - Review
4. Save the cleaned data to a new CSV file
    - Save cleaned dataset as processed data
    - Use descriptive statistics to understand the data
    - Review
5. Explore Data and Visualise
    - Statistics
    - Probability
    - Create visualisations based on sales, customers and products to identify trends and patterns for key insights, conclusions, recommendations and improvements
    - Create RFM cluster analysis to identify customer categories
    - Test hypotheses using T Test
    - Create visualisations in line with hypotheses, detailing key insights, conclusions, recommendations and improvements.
    - Commentary on ethical and societal considerations for each hypothesis
    - Overall conclusion
    - Ethical, legal and social considerations
    - Final thoughts
    - Future Developments
    - Store still images in the appropriate folders (plotly charts)
    - Review
6. Dashboard Creation
    - Use a wireframe and Tableau to plan and create an interactive dashboard that includes key metrics and visualisations in line with the hypotheses
    - Publish Dashboard
    - Store screengrabs of the wireframe and dashboard in the appropriate folders
    - Review
7. README
    - Write comprehensive README document
    - Store KanBan phases images in the appropriate folder
    - Review
8. Submit Project
    - Review 
    - Submit project

## The rationale to map the business requirements to the Data Visualisations

- Enhance Customer Retention and Engagement.
- Enhance Marketing and Strategy for High Value Customers (loyalty & Reward Schemes).
- Optimise Product Offerings and Inventory Management.
- Drive Expansion To Other Regions.
- Drive Strategic Sales Growth.

These business objectives are achieved by thoroughly understanding the data through processing and visualisation. This approach provides actionable insights and potential solutions to meet the business requirements.

In the retail industry, it is common practice to analyse sales trends, seasonality, customer spending behaviours, region exposure and product preferences to inform decision making and drive business success.

## Analysis techniques used

**List of techniques used**

ETL Notebook:

- df.duplicated().sum() was used to check for duplicate data.
- df.drop_duplicates() was used to drop duplicate data.
- Converted datatypes to the appropriate types.
- df_info was used to provide an overview of the dataset, list of columns and missing values.
- dropna was used to remove missing values and isnull().sum() to check column for missing values.
- Added a new column in the dataset which consisted of Quantity * UnitPrice.
- info() to provide a summary of the dataset.
- str.contains(r'\?' was used to remove cells which included special characters.
- str.contains(r'[a-z] was used to remove cells which included lower case letters.
- stats_summary was used to provide descriptive statistics.
- to_csv was used to save the clean dataset.
- pd.read_csv was used to load the clean dataset.

Data Visualisation Notebook:

- describe() was used for statistical summary.
- Matplotlib was used to plot a pie chart for probability findings.
- ttest_1samp was used for t testing to obtain p value and t-statistics.
- Hisplot chart used to display distribution of transaction values.
- Matplotlib line+bar chart was used for monthly trend analysis.
- Plotly pie chart was used for sales by day analysis.
- groupby was used in various analysis to group elements together such as CustomerID and Quantity.
- Subplots and axes was used to create 3 visualisation on 1 line displaying top 6 customers by quantity, unit price and then total transaction value.
- Kmeans.fit_predict was used for RFM clustering.
- Scatterplots was used for popular products charts quantity and total transaction value.
- Plotly line chart was used to display the top 6 product sales trend over 13 months.
- ttest_ind was used to validate all 3 hypotheses.
- Boxplot was used to display Customer Spending Comparison: UK vs Non-UK.
- Bar chart was used to display Average Revenue: Weekdays vs Weekends.
- Bar chart was used to display Average Transaction Value: Holiday vs Non-Holiday Months.

I structured the data analysis techniques to include as much variation as possible from the LMS i.e. charts were used across the board of seaborn, matplotlib and plotly. I ensured that i had something to include for each method as well as picking out the best techniques related to what i wanted to produce.

I did decide against an area chart for the customers section as it visually looked messy, therefore i opted for a simple bar charts. bar charts gave me the visual i needed, very simple, clear and concise.

I did decide against creating a visual representation of the RFM cluster of customers in addition to the tabled results. a visualisation was created, however the visual did not bring much inform forward by just looking at it. Therefore i decided to summarise this section with key insights, conclusion, suggest recommendations and improvements, and ethical and social considerations.

I did have some challenges in deciding what types of charts i wanted to use for my confirmed sections within the data_visualisation notebook. However i used AI to provide me with the benefits and downfalls of using particular charts. I then was able to make a decision on the best fit charting for the circumstance.

I used AI with ideation in relation to understanding what elements are heavily viewed for an online retail business. I was also able to research and obtain information in regards to business goals and objectives ideas. I was then able to build my business requirements and hypotheses. Using AI, i was able to decide what visualisations i wanted to create for an online retailer. 

I used AI to understand some coding scripts to gain some knowledge and better understanding on how it works such as ttest and probability.

Some written content was refined using AI to achieve a more formal and academic style.

## Ethical considerations

- The online retail dataset came from Kaggle and does not have any legal or societal issues. There was no personal data within the dataset which could expose or identify anything personal to a particular individual.
- Within the ETL notebook, i have included ethical, legal and social implications for data handling.
- Within the data_visualisation notebook, i have included ethical and societal considerations commentary under each hypothesis and RFM customer analysis.

## Wireframe

- The dashboard wireframe was created in Figma to outline the layout for the dashboard. It includes key components, such as summary cards for quick key points and charts (line, bar, pie and map). This wireframe will serve as a guide while designing the interactive dashboard.

**Wireframe Design:**

![alt text](assets/wireframe/Wireframe_Design.png)

## Dashboard Design

The dashboard was designed to be visually appealing, with a heavy set of key insights and charts to display valuable information.

A consistent blue-teal colour scheme was applied to the dashboard to reduce visual clutter and maintain a clean, cohesive look across all visual elements. This choice not only improves readability, especially in a data rich interfaces, but also supports accessibility as blue-teal tones are generally distinguishable for individuals with common types of colour blindness. This layout enhances the user experience. 

The dashboard design did not replicate the wireframe design in full. After metrics had been created, when it came to placement of the metrics using the wireframe guideline, through review, adjustments were made to ensure readbaility and reduce clutter. Further metrics were created as previous ones did not fit well with the design i wanted or added visual clutter. 

**Online Retail Dashboard** 

This is the main dashboard that represents the summary of the data for example, total revenue, invoices, quantity sold, total number of customers.

Visualisations on the dashboard that was chosen to provide valuable insights are listed below:

- Monthly Revenue and Quantity Trend Analysis (Bar+Line Chart).
- Top 6 Product Sales Trend Analysis (Line Chart).
- Revenue Regions (Map).
- Quarterly Rev & Quantity (Packed Bubbles Chart).
- Top 6 Customers by Revenue (Bar Chart).

All charts have clear titles, labels, and legends to ensure that users can easily understand the information being presented. Interactive elements, such as filters and tooltips, allow users to explore the data in more detail and gain deeper insights.

Worksheet list below:

- Revenue Regions
- Quarterly Rev & Quantity
- Monthly Revenue Trend Analysis
- Top 6 Product Sales Trend Analysis
- Top 6 Customers by Quantity
- Top 6 Customers by Revenue
- Total Revenue
- Total Quantity
- Total Customers
- Invoice Count
- Top 6 Customers - Quantity
- Top 6 Customers - Rev
- Monthly Revenue and Quantity Trend Analysis

Dashboard list:

- Online Retail Dashboard Preview:
![alt text](dashboard/Dashboard.png)

## Kanban Board
-  You can find the project board [here](https://github.com/users/mobess12/projects/3/views/1)
- You can find multiple screengrabs of the project board within the "kanban" folder which is located in the "assets" folder.

**MoSCoW**

The MoSCoW method was used in this project as a framework for prioritising tasks. It helps distinguish between critical and non-essential requirements, ensuring that key objectives are addressed first and project resources are allocated effectively to what matters most for success. 

- **Must Have**: Non-negotiable items essential for the project's success. 

- **Should Have**:Important features that add significant value but are not essential for immediate delivery.

- **Could Have**: Desirable features that are not necessary but would be nice to have if time and resources allow. 

- **Won't Have**: Features that are not a priority for the current timeframe.

You can find this methodology being used for issues [here](https://github.com/users/mobess12/projects/3/views/2?visibleFields=%5B%22Title%22%2C%22Assignees%22%2C%22Status%22%2C%22Labels%22%5D)

Preview:
![alt text](assets/kanban/KanBan_4.png) 

## Unfixed Bugs
- I don't have any unfixed bugs in this project to my knowledge.

## Development Roadmap

- I did not encounter any major issues. I had offered out my help to others and luckily for me, student colleagues offered me advice and provided further knowledge if i needed it. 

- Given I have come across issues in the past through this bootcamp, a lot of the issues that may have arised were rectified and newly learnt prior. Therefore referring back to experience, notes, LMS content and Google and colleagues in these situations was the solution.

- I have never done a wireframe design prior to this project, however I asked for advice off a colleague which essentially gave me the knowledge to build a customer wireframe.

- I have never created a full Tableau dashboard prior to this project, however have been involved in some elements of it and have knowledge of Power BI. In this project I chose to use Tableau to challenge myself and gain experience in another dashboarding tool. I built the entirety of the dashboard on my own and using resources such as YouTube and Google as a FAQ engines aided where it was needed.

- I want to experience more with VSCode and Tableau as I can see the benefits it can bring to data analytics. 

- I aim to continue practicing python on VSCode and building small to medium projects, while using Tableau to produce dashboards. This will give me more hands on experience and skill development for the future. 

## Deployment
### Tableau

- You can find a link to our dashboard [here] DO NOT FORGET TO LINK URL 

## Main Data Analysis Libraries

- Pandas
- NumPy
- Matplotlib
- Seaborn
- Plotly
- SKLearn
- Scipy.Stats

## Credits 

- LMS via Code Institute
- Google
- YouTube
- StackedOverflow
- GeeksForGeeks
- Datacamp
- Medium
- PlotlyCommunityForum
- Chat GPT and other AI engines
- Co-Pilot
- Facilitators
- Colleagues
- VSCode
- Github
- Tableau

## Acknowledgements 
- Vasi
- Neil
- Student Colleagues