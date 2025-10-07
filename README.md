# Project XYZ

**Project XYZ** is a comprehensive data analysis tool designed to streamline data exploration, analysis, and visualisation. The tool supports multiple data formats and provides an intuitive interface for both novice and expert data scientists.

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
* Describe your business requirements


## Hypothesis and how to validate?
* List here your project hypothesis(es) and how you envision validating it (them) 

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
    - Test hypotheses using T Test
5. Dashboard Creation
    - Use a wireframe and DASHBOARD TOOL to plan and create an interactive dashboard that includes key metrics and visualisations in line with the hypotheses


## The rationale to map the business requirements to the Data Visualisations
* List your business requirements and a rationale to map them to the Data Visualisations

## Analysis techniques used
* List the data analysis methods used and explain limitations or alternative approaches.
* How did you structure the data analysis techniques. Justify your response.
* Did the data limit you, and did you use an alternative approach to meet these challenges?
* How did you use generative AI tools to help with ideation, design thinking and code optimisation?

## Ethical considerations
- The online retail dataset came from Kaggle and does not have any legal or societal issues. There was no personal data within the dataset which could expose or identify anything personal to a particular individual.

## Dashboard Design
* List all dashboard pages and their content, either blocks of information or widgets, like buttons, checkboxes, images, or any other item that your dashboard library supports.
* Later, during the project development, you may revisit your dashboard plan to update a given feature (for example, at the beginning of the project you were confident you would use a given plot to display an insight but subsequently you used another plot type).
* How were data insights communicated to technical and non-technical audiences?
* Explain how the dashboard was designed to communicate complex data insights to different audiences. 

## Kanban Board
-  You can find the project board [here](https://github.com/users/mobess12/projects/3/views/1)


## Unfixed Bugs
* Please mention unfixed bugs and why they were not fixed. This section should include shortcomings of the frameworks or technologies used. Although time can be a significant variable to consider, paucity of time and difficulty understanding implementation are not valid reasons to leave bugs unfixed.
* Did you recognise gaps in your knowledge, and how did you address them?
* If applicable, include evidence of feedback received (from peers or instructors) and how it improved your approach or understanding.

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

## Credits 

* In this section, you need to reference where you got your content, media and extra help from. It is common practice to use code from other repositories and tutorials, however, it is important to be very specific about these sources to avoid plagiarism. 
* You can break the credits section up into Content and Media, depending on what you have included in your project. 

### Content 

- The text for the Home page was taken from Wikipedia Article A
- Instructions on how to implement form validation on the Sign-Up page was taken from [Specific YouTube Tutorial](https://www.youtube.com/)
- The icons in the footer were taken from [Font Awesome](https://fontawesome.com/)

## Acknowledgements (optional)
* Thank the people who provided support through this project.