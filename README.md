# Hospitality-Analytics

Domain:  Hospitality       Function: Revenue

  AtliQ Grands owns multiple five-star hotels across India. They have been in the hospitality industry for the past 20 years. 
  Due to strategic moves from other competitors and ineffective decision-making in management, AtliQ Grands are losing its 
  market share and revenue in the luxury/business hotels category. As a strategic move, the managing director of AtliQ Grands
  wanted to incorporate “Business and Data Intelligence” to regain their market share and revenue. However, they do not have
  an in-house data analytics team to provide them with these insights.

  Their revenue management team had decided to hire a 3rd party service provider to provide them with insights from their 
  historical data.

# Task:  

  Here is a brief overview of the workflow for the task:

    1. Review the data.
    2. Metrics list :
       • Revenue
       • Total Bookings
       • Average Rating
       • Total Capacity
       • Total Successful Bookings
       • Occupancy % 
       • Total Cancelled Bookings
       • Cancellation Rate
       • RevPar (Revenue Per Available Room)
       • ADR (Average Daily Rate)
       • ADR (Average Daily Rate)
       • SRN (Sellable Room Nights)
       • DSRN (Daily Sellable Room Nights)
       • Realization
       • URN (Utilized Room Nights)
       • BRN (Booked Room Nights)
     Key Metrics :
       • RevPar 
       • Occupancy %
       • Revenue
       • DSRN
       • ADR
       • Realization 
--------------------------------------------------------------------------------------------------------------------------------

# Step 1 : Data Collection and Preparation

Import Datasets into Power BI

# Step 2 : Data Exploration and Analysis

• Duplicate the files one by one and then expand it use the similar approach for all the other files.

• Promote the first row as header if its needed for the dim_rooms table.

# Removing a Column For Weekdays and Weekends

• In the dim_date table, based on discussions with the subject matter expert in the hotel industry, Friday and Saturday
  are considered weekends. However, the table currently defines weekends as Saturday and Sunday.

![image_alt](https://github.com/DSgenes/Hospitality-Analytics/blob/381c572afbb4159a7f539a55c4058f727d73941c/Screenshot%201.png)

• Right-click on the day_type column and select Remove to delete it. It is not needed.

![image_alt](https://github.com/DSgenes/Hospitality-Analytics/blob/381c572afbb4159a7f539a55c4058f727d73941c/Screenshot%202.png)

• It's a good practice to name steps as needed.

![image_alt](https://github.com/DSgenes/Hospitality-Analytics/blob/7d453b54afd3167a098ad735f42df89a524ee54c/Screenshot%203.png)

• Close & Apply to save the changes.

# Data Modeling

• In data modeling, the star schema is used to organize data where the fact tables are placed at the center, containing measurable,
quantitative data such as sales, revenue, or occupancy rates. Surrounding the fact tables are dimension tables 
(prefixed with "dim_"), which contain descriptive attributes related to the facts.

![image_alt](https://github.com/DSgenes/Hospitality-Analytics/blob/9fe9f4b1a9ef29362a34899dad548ce5d5347cc9/Screenshot%204.png)

![image_alt](https://github.com/DSgenes/Hospitality-Analytics/blob/9fe9f4b1a9ef29362a34899dad548ce5d5347cc9/Screenshot%205.png)

# Building Metrics Using Dax

# Adding a Column for Weekday and Weekend

• In the dim_date table, you can create a new column to extract the week number without the 'W' prefix. You can either
  modify the existing column by removing the 'W', or simply create a new column that directly derives the week number 
  from the date column. To do this, go ahead and create a new column with the formula:

  ![image_alt](https://github.com/DSgenes/Hospitality-Analytics/blob/44a7f04c2c6edf1205c2b09453f561c3c04840ba/Screenshot%206.png)

• To classify Friday and Saturday as weekends, use the following DAX formula:

![image_alt](https://github.com/DSgenes/Hospitality-Analytics/blob/c9cdd18999b54b5cc1989aff85bec8f15e7933e1/Screenshot%207.png)

  This formula labels Friday (6) and Saturday (7) as Weekend, while Sunday through Thursday are labeled as Weekday,
  based on the hotel industry standards discussed. We'll expand this formula by using this DAX Expression : 

![image_alt](https://github.com/DSgenes/Hospitality-Analytics/blob/c9cdd18999b54b5cc1989aff85bec8f15e7933e1/Screenshot%208.png)

# Creating a Table for Measures 

![image_alt](https://github.com/DSgenes/Hospitality-Analytics/blob/7833ebc83e21f21ebc639fb90f1c268853b74f68/Screenshot%209.png)

# Creating Measures By Using Formulas

# Create Revenue Measure

• Click the ellipsis besides the Key Measures Table ➜ Create a new measure 

![image_alt](https://github.com/DSgenes/Hospitality-Analytics/blob/7833ebc83e21f21ebc639fb90f1c268853b74f68/Screenshot%2010.png)

• Build a card visual.

![image_alt](https://github.com/DSgenes/Hospitality-Analytics/blob/185ba6027f79850d3439c104cd590799c63d2133/Screenshot%2011.png)

• Show some decimal points.

![image_alt](https://github.com/DSgenes/Hospitality-Analytics/blob/2ae366ae8a6b2f07bf1634ef883392023d4c2ec7/Screenshot%2012.png)

• Let's say this is my total revenue. Do a quick verification using Excel sheets for this.

    • Go to Excel Sheets : fact_bookings.csv ➜ Put your cursor to the Row no. 2 in the revenue_realized column then press 
                             Ctrl + Shift + ↓ 
      and it'll select the whole column. At the bottom, it'll show the sum of that number and the number
      is exactly the same as its in Power bi Card Visual.

# Create Total Bookings Measure

![image_alt](https://github.com/DSgenes/Hospitality-Analytics/blob/2ae366ae8a6b2f07bf1634ef883392023d4c2ec7/Screenshot%2013.png)

# Create Total Capacity Measure

![image_alt](https://github.com/DSgenes/Hospitality-Analytics/blob/2ae366ae8a6b2f07bf1634ef883392023d4c2ec7/Screenshot%2014.png)

# Create Total Successful Bookings 

![image_alt](https://github.com/DSgenes/Hospitality-Analytics/blob/2ae366ae8a6b2f07bf1634ef883392023d4c2ec7/Screenshot%2015.png)

#   Note : Create all the other measures using the same approach as provided in the excel file metrics list (1).xlsx 
#          with detailed description.

![image_alt]()

    
