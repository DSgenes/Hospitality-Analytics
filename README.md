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

![image_alt]()

  This formula labels Friday (6) and Saturday (7) as Weekend, while Sunday through Thursday are labeled as Weekday,
  based on the hotel industry standards discussed. We'll expand this formula by using this DAX Expression : 

![image_alt]()

![image_alt]()

![image_alt]()
