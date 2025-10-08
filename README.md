# **Online Retail Analysis - Capstone Project**

Online Retail Analysis is a data-driven tool designed to support business decision making through comprehensive analysis and visualisation. Built with Python and key libraries including Pandas, Plotly, Seaborn, Matplotlib, SKLearn, a Dashboarding tool, the tool ingests raw CSV data, processes it efficiently, and delivers actionable insights via interactive visualizations in both Jupyter Notebook and dashboards.

# ![CI logo](https://codeinstitute.s3.amazonaws.com/fullstack/ci_logo_small.png)


## Dataset Content

Online Retail Dataset can be found [here]( https://www.kaggle.com/datasets/abhishekrp1517/online-retail-transactions-dataset)

The online retail dataset contains transactional data of 13 months, including product details, quantities, prices, purchase timestamps, customer IDs, and country information. It can be used to analyse customer behavior, identify popular products, and support pricing and marketing strategies. It's suitable for data analysis and machine learning. 

Column Descriptors

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


## Hypothesis and how to validate?

Hypothesis 1 - Customers in the United Kingdom spend more than those not in the United Kingdom per transaction

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
2. Data Cleaning and Preprocessing
    - Investigate dataset on Microsoft Excel
    - Handle null values, remove duplicates, and correct data types to appropriate ones 
    - Remove irrelevant data (e.g., transactions with negative quantities, product descriptions that are not products such as "damages and ?")
    - Create new features Total Transaction Value (Quantity*UnitPrice)
3. Save the cleaned data to a new CSV file
    - Save cleaned dataset as processed data
    - Use descriptive statistics to understand the data
4. Explore Data and Visualise
    - Create visualisations based on sales, customers and products to identify trends and patterns for key insights, conclusions, recommendations and improvements
    - Create RFM cluster analysis to identify customer categories
    - Create visualisations in line with hypotheses, detailing key insights, conclusions, recommendations and improvements.
    - Commentary on ethical and societal considerations for each hypothesis
    - Test hypotheses using T Test
5. Dashboard Creation
    - Use a wireframe and DASHBOARD TOOL to plan and create an interactive dashboard that includes key metrics and visualisations in line with the hypotheses

## The rationale to map the business requirements to the Data Visualisations

- Enhance Customer Retention and Engagement
- Enhance Marketing and Strategy for High Value Customers (loyalty & Reward Schemes)
- Optimize Product Offerings and Inventory Management
- Drive Expansion To Other Regions
- Drive Strategic Sales Growth

These business objectives are achieved by thoroughly understanding the data through processing and visualisation. This approach provides actionable insights and potential solutions to meet the business requirements.

In the retail industry, it is common practice to analyse sales trends, seasonality, customer spending behaviours, region exposure and product preferences to inform decision making and drive business success.

## Analysis techniques used

**List of techniques used**

ETL Notebook:

- df.duplicated().sum() was used to check for duplicate data
- df.drop_duplicates() was used to drop duplicate data
- Converted datatypes to the appropriate types
- df_info was used to provide an overview of the dataset, list of columns and missing values
- dropna was used to remove missing values and isnull().sum() to check column for missing values
- Added a new column in the dataset which consisted of Quantity * UnitPrice
- info() to provide a summary of the dataset
- str.contains(r'\?' was used to remove cells which included special characters
- str.contains(r'[a-z] was used to remove cells which included lower case letters
- stats_summary was used to provide descriptive statistics
- to_csv was used to save the clean dataset
- pd.read_csv was used to load the clean dataset

Data Visualisation Notebook:

- describe() was used for statistical summary
- ttest_1samp was used for t testing to obtain p value and t-statistics
- Hisplot chart used to display distribution of transaction values
- Matplotlib line+bar chart was used for monthly trend analysis
- Plotly pie chart was used for sales by day analysis
- groupby was used in various analysis to group elements together such as CustomerID and Quantity
- subplots and axes was used to create 3 visualisation on 1 line displaying top 6 customers by quantity, unit price and then total transaction value
- kmeans.fit_predict was used for RFM clustering
- Scatterplots was used for popular products charts quantity and total transaction value
- plotly line chart was used to display the top 6 product sales trend over 13 months
- ttest_ind was used to validate all 3 hypotheses
- Boxplot was used to display Customer Spending Comparison: UK vs Non-UK
- Bar chart was used to display Average Revenue: Weekdays vs Weekends
- Bar chart was used to display Average Transaction Value: Holiday vs Non-Holiday Months

I structured the data analysis techniques to include as much variation as possible from the LMS i.e. charts were used across the board of seaborn, matplotlib and plotly. I ensured that i had something to include for each method as well as picking out the best techniques related to what i wanted to produce.

I did decide against an area chart for the customers section as it visually looked messy, therefore i opted for a simple bar charts. bar charts gave me the visual i needed, very simple, clear and concise.

I did have some challenges in deciding what types of charts i wanted to use for my confirmed sections within the data_visualisation notebook. However i used AI to provide me with the benefits and downfalls of using particular charts. I then was able to make a decision on the best fit charting for the circumstance.

I used AI with ideation in relation to understanding what type of elements are heavily viewed for an online retail dataset. I was then able to build my business requirements and hypotheses. I also used AI for deciding what areas of online retail i wanted to produce visualisations for i.e. what is the key importance or insight. I also used AI to understand some coding scripts to gain some knowledge and better understanding on how it works i.e. ttest.

## Ethical considerations
- The online retail dataset came from Kaggle and does not have any legal or societal issues. There was no personal data within the dataset which could expose or identify anything personal to a particular individual.
- Within the data_visualisation notebook, i have included ethical and societal considerations commentary under each hypothesis.

## Wireframe

- The dashboard wireframe was created in Figma to outline the layout for the dashboard. It includes key components, such as summary cards for quick key points and charts (line, bar, pie and map). This wireframe will serve as a guide while designing the interactive dashboard.

**Wireframe Design:**

![alt text](assets/wireframe/Wireframe_Design.png)

## Dashboard Design
* List all dashboard pages and their content, either blocks of information or widgets, like buttons, checkboxes, images, or any other item that your dashboard library supports.
* Later, during the project development, you may revisit your dashboard plan to update a given feature (for example, at the beginning of the project you were confident you would use a given plot to display an insight but subsequently you used another plot type).
* How were data insights communicated to technical and non-technical audiences?
* Explain how the dashboard was designed to communicate complex data insights to different audiences. 

## Kanban Board
-  You can find the project board [here](https://github.com/users/mobess12/projects/3/views/1)
- You can find multiple screengrabs of the project board in the "kanban" folder within the "assets" folder.

**MoSCoW**

The MoSCoW method was used in this project as a framework for prioritising tasks. It helps distinguish between critical and non-essential requirements, ensuring that key objectives are addressed first and project resources are allocated effectively to what matters most for success. 

- Must Have: Non-negotiable items essential for the project's success. 

- Should Have:Important features that add significant value but are not essential for immediate delivery.

- Could Have: Desirable features that are not necessary but would be nice to have if time and resources allow. 

- Won't Have: Features that are not a priority for the current timeframe.

You can find this methodology being used in the screengrab "KanBan_4.PNG" which is located in the folder "kanban" under "assets" folder.

## Unfixed Bugs
- I don't have any unfixed bugs in this project to my knowledge.

## Development Roadmap
* What challenges did you face, and what strategies were used to overcome these challenges?
* What new skills or tools do you plan to learn next based on your project experience? 

## Deployment
### Heroku

* The App live link is: https://YOUR_APP_NAME.herokuapp.com/ 
* Set the runtime.txt Python version to a [Heroku-20](https://devcenter.heroku.com/articles/python-support#supported-runtimes) stack currently supported version.
* The project was deployed to Heroku using the following steps.

1. Log in to Heroku and create an App
2. From the Deploy tab, select GitHub as the deployment method.
3. Select your repository name and click Search. Once it is found, click Connect.
4. Select the branch you want to deploy, then click Deploy Branch.
5. The deployment process should happen smoothly if all deployment files are fully functional. Click now the button Open App on the top of the page to access your App.
6. If the slug size is too large then add large files not required for the app to the .slugignore file.


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

## Acknowledgements (optional)
- Vasi
- Neil
- Student Colleagues