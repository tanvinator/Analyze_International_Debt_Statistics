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
      In order to get unique values of debt indicators, indicator_code column is used. 
      The result is arranged alphabetically using the ORDER BY clause.

  ### Inference

    There are 25 distinct debt indicators listed in the database, which are arranged alphabetically.
    
<img width="507" alt="image" src="https://user-images.githubusercontent.com/58279797/153733138-72c4ef0c-c24d-4326-8fef-6edeba97af17.png">
<img width="89" alt="image" src="https://user-images.githubusercontent.com/58279797/153733155-25563a3c-1e14-4ae8-95d3-b66e36cf34de.png">

## **3. Totalling the amount of debt owed by the countries**

As mentioned earlier, the financial debt of a particular country represents its economic state. But if we were to project this on an overall global scale, how will we approach it?

Let's switch gears from the debt indicators now and find out the total amount of debt (in USD) that is owed by the different countries. This will give us a sense of how the overall economy of the entire world is holding up.

  ### Approach:
    The functions to be used are 

      SUM: Gives the total sum of values of the argument.

      ROUND: Rounds up the value to specified number of decimals, 2 in this case.

  ### Inference

    The total debt owed by all the countries to the World bank (reduced scale by 1000000) is USD 3079734.49 ONLY.
    
<img width="504" alt="image" src="https://user-images.githubusercontent.com/58279797/153733343-4e63436d-dc3a-43ad-88b7-e5c62f0425a1.png">


## **4. Country with the Highest debt**

"Human beings cannot comprehend very large or very small numbers. It would be useful for us to acknowledge that fact." - Daniel Kahneman. That is more than 3 million million USD, an amount which is really hard for us to fathom.

Now that we have the exact total of the amounts of debt owed by several countries, let's now find out the country that owns the highest amount of debt along with the amount. Note that this debt is the sum of different debts owed by a country across several categories. This will help to understand more about the country in terms of its socio-economic scenarios. We can also find out the category in which the country owns its highest debt. But we will leave that for now.

  ### Approach:
  
    Aggregate function SUM can be used to group the debts based on the country names, using the GROUP BY clause.
    ORDER BY ... DESC can be used to order the debts in a descending order.

  ### Inference

    The country with the highest debt is China, with the total debt of USD 285793494734.20.
    
<img width="506" alt="image" src="https://user-images.githubusercontent.com/58279797/153734737-3a58ab96-49a9-4efc-b35a-9e05319136cf.png">


## **5. Average amount of debts across indicators**

So, it was China. A more in-depth breakdown of China's debts can be found here.

We now have a brief overview of the dataset and a few of its summary statistics. We already have an idea of the different debt indicators in which the countries owe their debts. We can dig even further to find out on an average how much debt a country owes? This will give us a better sense of the distribution of the amount of debt across different indicators.
  
  ### Approach:
    Aggregate function AVG can be used to group the debts based on the debt indicator, using the GROUP BY clause.
    ORDER BY ... DESC can be used to order the debts in a descending order.

  ### Inference

    Top 10 debt indicators are listed with respective average debts in that category.
    
<img width="505" alt="image" src="https://user-images.githubusercontent.com/58279797/153734966-ae76cfe3-8c92-4873-94a5-64938fb0c5fc.png">
















