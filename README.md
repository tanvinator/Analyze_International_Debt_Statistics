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

<img width="506" alt="image" src="https://user-images.githubusercontent.com/58279797/153732853-481eec91-3537-46ac-b5ae-b76cc1328290.png">






