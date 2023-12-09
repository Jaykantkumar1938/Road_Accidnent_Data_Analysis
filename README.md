# Driving Insights with Power BI: The Road Accident Data Project

Initiative aimed at analyzing and understanding the alarming rise of road accidents in our modern world. This pioneering endeavor delves into the statistical landscape of traffic incidents, leveraging advanced data analysis techniques to uncover crucial patterns and insights. By examining factors such as location, date, areas, and vehicle types, this project seeks to inform policymakers, transportation authorities, and communities alike, empowering them to implement effective measures and create safer roads for all.

 ![image](https://github.com/Jaykantkumar1938/Road_Accidnent_Data_Analysis/assets/132810111/89aba8b9-7efe-4c48-98f2-91189eac7247)

The dataset utilized in this project was sourced from the reputable Kaggle website. It comprises a practice-oriented demonstration dataset, featuring 21 columns and 307,973 rows. The primary objectives of this project encompass identifying trends, offering valuable insights regarding casualties, and addressing the following key Metrics
![image](https://github.com/Jaykantkumar1938/Road_Accidnent_Data_Analysis/assets/132810111/248972a0-dfbe-4ece-ac7f-5972ca604862)



The data was downloaded and opened in Power Bi below is the data set view




steps i took to Analyze the data 

# Data cleaning 
promoted headers

checked for data consistency -changed data type ,I checked the data type based on the field name i.e. the “Accident_index” — Text format, “Accident_Date” — Date format, etc.

I checked further and I noticed another misspelled word in the “Accident_Severity” column we have “Fetal” instead of “Fatal” using Replace value on data tab

![image](https://github.com/Jaykantkumar1938/Road_Accidnent_Data_Analysis/assets/132810111/c887d9a2-7f93-4903-b453-c08add313adf)
![image](https://github.com/Jaykantkumar1938/Road_Accidnent_Data_Analysis/assets/132810111/5f0bfd97-dab1-444b-b472-5a6e6da355c2)
![image](https://github.com/Jaykantkumar1938/Road_Accidnent_Data_Analysis/assets/132810111/ab8401ae-fada-412b-b7f1-5c05620588e0)




# Analyzing the Data
After completing the data cleaning process, I proceeded to analyze the data.

The first step in analyzing the data was to create a table that included the calendar dates in reference to the above metrics, including both current and previous year information

“I inputted the calendar date into Power BI using the Calendar AUTO function” or “I utilized the Calendar AUTO feature in Power BI to input the calendar date.”

“The images below depict the process I took

![image](https://github.com/Jaykantkumar1938/Road_Accidnent_Data_Analysis/assets/132810111/7dd6480c-d15b-4b17-8a80-04506bb5f458)


“To obtain the dates in the dataset, I utilized the formula ‘CALENDAR(MIN(Data[Accident Date]), MAX(Data[Accident Date]))’.”

This conveys that you used the “CALENDAR” function in Power BI, specifying the minimum and maximum dates from the “Accident Date” column in the “Data” table to generate a calendar range.

![image](https://github.com/Jaykantkumar1938/Road_Accidnent_Data_Analysis/assets/132810111/434792ad-dee3-4d6a-8a6f-d8a9388e3f9b)


I added another column to the calendar date table called ‘Year’ by using the formula ‘YEAR(calendar[Date].[Date])’.”

“YEAR” function in Power BI to extract the year from the ‘Date’ column in the ‘calendar’ table, and created a new column named ‘Year’ in the calendar date table based on that calculation.

![image](https://github.com/Jaykantkumar1938/Road_Accidnent_Data_Analysis/assets/132810111/9a581108-890d-4d31-ac72-ac087aa31c3b)


inserted the function above to extract the month from date column

The image below depicts an overview of the calendar date table:”


![image](https://github.com/Jaykantkumar1938/Road_Accidnent_Data_Analysis/assets/132810111/8c0020f1-fcf0-4f0b-9a44-7fc254c83d57)


I proceeded to provide answers and insights for the above metrics.

Total Casualties and Total Accident values for current Year

current Year Casualties (CY)2022


![image](https://github.com/Jaykantkumar1938/Road_Accidnent_Data_Analysis/assets/132810111/b7710156-2b1d-464b-9ef8-57541b8328b6)


“TOTALYTD”calculate the year-to-date sum of the ‘Number_of_Casualties’ column from the ‘Data’ table based on the ‘Date’ column in the ‘calendar’ table. The result is the count of casualties for the current year.

![image](https://github.com/Jaykantkumar1938/Road_Accidnent_Data_Analysis/assets/132810111/2d98bbfa-920e-404c-b589-c3c60d4c7d72)


The Total casualties recorded for the year 2022 is 196,000.


![image](https://github.com/Jaykantkumar1938/Road_Accidnent_Data_Analysis/assets/132810111/f42d3dfa-e2fa-4ce7-9fd7-efa75d6679cb)



“TOTALYTD”calculate the year-to-date count of accident indices from the ‘Data’ table based on the ‘Accident Date’ column, resulting in the current year casualties




![image](https://github.com/Jaykantkumar1938/Road_Accidnent_Data_Analysis/assets/132810111/0ccd9c05-ffad-4846-b928-760ef3a6706a)




Total Accident recorded for 2022 is 144,000

(2) Total Casualties by Accident Severity For Current Year

>Fatal


![image](https://github.com/Jaykantkumar1938/Road_Accidnent_Data_Analysis/assets/132810111/e54024c9-5778-42ad-9a80-9254f177ee3b)




specifying the condition that the ‘Accident_Severity’ column should be equal to “Fatal” to filter the data and obtain the count of fatal casualties based on the previously calculated ‘CY casualties’.


![image](https://github.com/Jaykantkumar1938/Road_Accidnent_Data_Analysis/assets/132810111/122bf8e1-c6ed-447e-a27f-dee3835278bd)



Total fatal casualties is 2900

> Slight


![image](https://github.com/Jaykantkumar1938/Road_Accidnent_Data_Analysis/assets/132810111/e0f6e438-c45d-48be-bd13-93d2d7eb4bd8)



specifying the condition that the ‘Accident_Severity’ column should be equal to “slight ” to filter the data and obtain the count of fatal casualties based on the previously calculated ‘CY casualties’.



![image](https://github.com/Jaykantkumar1938/Road_Accidnent_Data_Analysis/assets/132810111/08c10526-4a25-468a-9b37-135714df25bf)



slight casualties is 166,000

>Serious


![image](https://github.com/Jaykantkumar1938/Road_Accidnent_Data_Analysis/assets/132810111/1a765b06-dd47-4a7f-a8c9-037e7af44460)



![image](https://github.com/Jaykantkumar1938/Road_Accidnent_Data_Analysis/assets/132810111/19175363-58a1-42fb-8b8b-30676164df5d)



Serious casualties is 27,000

(3) Total Casualties with respect to Vehicle Type for current Year

In order to analyze casualties by vehicle type, I grouped certain categories together. For the ‘Cars’ category, I combined ‘Car’ and ‘Taxi/Private hire car’ into a single group. Similarly, for the ‘Bus’ category, I merged ‘Bus or coach (17 or more pass seats)’ with ‘Minibus (8–16 passenger seats)’.

I followed a similar approach for other categories as well. In the ‘Van’ category, I combined ‘Goods 7.5 tonnes mgw and over’, ‘Goods over 3.5t and under 7.5t’, and ‘Van/Goods 3.5 tonnes mgw or under’.

For the ‘Motorcycle’ category, I grouped ‘Motorcycle 125cc and under’, ‘Motorcycle 50cc and under’, ‘Motorcycle over 125cc and up to 500cc’, and ‘Motorcycle over 500cc’ together.

In the ‘Others’ category, I combined ‘Other vehicle’, ‘Pedal cycle’, and ‘Ridden horse’.

Finally, the ‘Agricultural vehicle’ category remained unchanged.”



![image](https://github.com/Jaykantkumar1938/Road_Accidnent_Data_Analysis/assets/132810111/9a02d0a2-b699-46bb-ac6d-ee7337b01e6d)



![image](https://github.com/Jaykantkumar1938/Road_Accidnent_Data_Analysis/assets/132810111/11a64d0a-749a-41e5-bfaf-e157f0c8c0de)




![image](https://github.com/Jaykantkumar1938/Road_Accidnent_Data_Analysis/assets/132810111/6b360655-fc8f-48cd-b0f0-6d2aba36e830)



In the current year(2022), the casualties by vehicle type were as follows: Agricultural Vehicles accounted for 399, Bikes accounted for 15,610, Buses accounted for 6,573, Cars accounted for 155,804, Others accounted for 1,446, and Vans accounted for 15,905.

(4)Monthly Trend Showing Comparison of casualties for Current Year and Previous Year

“To obtain the casualties for the previous year (2021), I employed the formula ‘CALCULATE(SUM(Data[Number_of_Casualties]), SAMEPERIODLASTYEAR(calendar[Date].[Date]))’.”

“To obtain the casualties for the previous year (2021), I employed the formula ‘CALCULATE(SUM(Data[Number_of_Casualties]), SAMEPERIODLASTYEAR(calendar[Date].[Date]))’.”



![image](https://github.com/Jaykantkumar1938/Road_Accidnent_Data_Analysis/assets/132810111/e7596a3e-5024-47e7-b3cb-6a5c8d90d644)



![image](https://github.com/Jaykantkumar1938/Road_Accidnent_Data_Analysis/assets/132810111/cf297026-7867-44b1-abb5-beea6a3841b1)



The table below presents insights on the monthly trend.



![image](https://github.com/Jaykantkumar1938/Road_Accidnent_Data_Analysis/assets/132810111/56a83bb8-6e0d-4f3e-b3fe-5310e2a658cf)



From the table, it is observed that there was an increase in the number of casualties only in the month of February for both the previous year (PY) and the current year (CY). In conclusion, the total number of casualties decreased in 2022.

Casualties By Road Type for Current Year


![image](https://github.com/Jaykantkumar1938/Road_Accidnent_Data_Analysis/assets/132810111/b7ab1ac7-e2b9-4cf0-848d-11e3f10ecc24)



single carriageways had the highest count of road casualties in the year 2022, specifically amounting to 145k

percentage of Current Year Casualties By Area



![image](https://github.com/Jaykantkumar1938/Road_Accidnent_Data_Analysis/assets/132810111/db3c1960-f36e-4f1c-a875-aeaab3f40ad2)




The above data shows that the Percentage of casualties in the urban area are more than the casualties in the rural area.

Percentage of Current Year Casualties by Day /Night

I observed that there were four different descriptions for the darkness/light condition. To simplify the analysis, I decided to group them into a single category called “Night” using a calculated item. This adjustment allows us to have two distinct categories for the light conditions: Day and Night.



![image](https://github.com/Jaykantkumar1938/Road_Accidnent_Data_Analysis/assets/132810111/cd1d095a-f15f-4380-8655-d724cd092bbf)



![image](https://github.com/Jaykantkumar1938/Road_Accidnent_Data_Analysis/assets/132810111/ed4571cb-1999-4b87-b9ee-9e12f0ffc1e5)





![image](https://github.com/Jaykantkumar1938/Road_Accidnent_Data_Analysis/assets/132810111/e0466b7b-ff26-4448-abb8-dff228d3d32d)




The data presented above indicates that the percentage of casualties during the day is higher than during the night.




# VISUALIZATION

All analysis can be viewed at a glance on the dashboard, providing a comprehensive overview in one place.



![image](https://github.com/Jaykantkumar1938/Road_Accidnent_Data_Analysis/assets/132810111/24e28f5c-73da-465b-b11b-e6e3be056869)

