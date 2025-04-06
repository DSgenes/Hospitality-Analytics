![image](https://github.com/user-attachments/assets/e8a40c86-35bd-49b9-b7af-0f6fa9db48f7)# Hospitality-Analytics

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

# Adding a Column For Weekdays and Weekends

• In the dim_date table, based on discussions with the subject matter expert in the hotel industry, Friday and Saturday
  are considered weekends. However, the table currently defines weekends as Saturday and Sunday.

![image_alt](https://github.com/DSgenes/Hospitality-Analytics/blob/381c572afbb4159a7f539a55c4058f727d73941c/Screenshot%201.png)

• Right-click on the day_type column and select Remove to delete it. It is not needed.

![image_alt](https://github.com/DSgenes/Hospitality-Analytics/blob/381c572afbb4159a7f539a55c4058f727d73941c/Screenshot%202.png)

• It's a good practice to name steps as needed.

![image_alt]()

• Close & Apply to save the changes.

![image_alt]()

![image_alt]()

