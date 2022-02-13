# **Project Description**

It's not that we humans only take debts to manage our necessities. A country may also take debt to manage its economy. For example, infrastructure spending is one costly ingredient required for a country's citizens to lead comfortable lives. The World Bank is the organization that provides debt to countries.

In this project, you are going to analyze international debt data collected by The World Bank. The dataset contains information about the amount of debt (in USD) owed by developing countries across several categories. You are going to find the answers to questions like:

What is the total amount of debt that is owed by the countries listed in the dataset?
Which country owns the maximum amount of debt and what does that amount look like?
What is the average amount of debt owed by countries across different debt indicators?
The data used in this project is provided by The World Bank. It contains both national and regional debt statistics for several countries across the globe as recorded from 1970 to 2015.

# **Skills applied**

1. Data Manipulation
2. Importing and Cleaning Data 

# **Dataset** 

The table international_debt can be found on the international_debt database, which can be accessed using SQL and Python in Jupyter Notebook. Access to the database is restricted. The sample table (first 10 rows) looks like this:

<img width="506" alt="image" src="https://user-images.githubusercontent.com/58279797/153732671-c8bef5cd-b667-40fd-b2a5-55ca4d0cd2ec.png">

# **Questions and Solutions:**
## **1. Finding the number of distinct countries**

From the first ten rows, we can see the amount of debt owed by Afghanistan in the different debt indicators. But we do not know the number of different countries we have on the table. There are repetitions in the country names because a country is most likely to have debt in more than one debt indicator.

Without a count of unique countries, we will not be able to perform our statistical analyses holistically. In this section, we are going to extract the number of unique countries present in the table.

  ### Approach:
    The functions to be used are 

      COUNT: Gives the total number of rows of the argument.

      DISTINCT: Filters out the unique values of the argument

  ### Inference

    There are 124 unique countries listed in the database.

<img width="506" alt="image" src="https://user-images.githubusercontent.com/58279797/153732853-481eec91-3537-46ac-b5ae-b76cc1328290.png">

## **2. Finding out the distinct debt indicators**

We can see there are a total of 124 countries present on the table. As we saw in the first section, there is a column called indicator_name that briefly specifies the purpose of taking the debt. Just beside that column, there is another column called indicator_code which symbolizes the category of these debts. Knowing about these various debt indicators will help us to understand the areas in which a country can possibly be indebted to.

  ### Approach:
      In order to get unique values of debt indicators, indicator_code column is used. The result is arranged alphabetically using the ORDER BY clause.

  ### Inference

    There are 25 distinct debt indicators listed in the database, which are listed alphabetically.
    
<img width="507" alt="image" src="https://user-images.githubusercontent.com/58279797/153733138-72c4ef0c-c24d-4326-8fef-6edeba97af17.png">
<img width="89" alt="image" src="https://user-images.githubusercontent.com/58279797/153733155-25563a3c-1e14-4ae8-95d3-b66e36cf34de.png">












