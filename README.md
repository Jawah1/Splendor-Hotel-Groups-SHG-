### Splendor-Hotel-Groups-SHG.

Through analysis of  the Splendor Hotel Groups (SHG) dataset, featuring intricate details of bookings, guest demographics, distribution channels, and financial metrics.
Using Microsoft Power BI

## Having gone through the data I will be using Microsoft Excel and Microsoft Power BI, to clean, analyze, and visualize the data.

I open the data in Excel to read through and understand the data.

![image](https://github.com/Jawah1/Splendor-Hotel-Groups-SHG-/assets/131864852/67b6ee96-1f6e-4855-8dec-4d2236e392dd)

Next, I imported the data on Powery to inspect the data type for each column to ensure they had the correct and I checked for inconsistency and dirty data and made sure of no errors or missing values

![image](https://github.com/Jawah1/Splendor-Hotel-Groups-SHG-/assets/131864852/e96f5c93-7349-461b-b5a0-0f979d538f23)

After doing some cleaning and preparation in power query, the data was saved and loaded into Power BI.

![image](https://github.com/Jawah1/Splendor-Hotel-Groups-SHG-/assets/131864852/c664b6d0-c54f-4a0a-b864-35933b053c3d)

 I created a calendar auto that consists of information such as Year, and month number.


I then used the sum function to get the total revenue then I created a model to calculate the total booking, this i did by using the distinct count function. 

![image](https://github.com/Jawah1/Splendor-Hotel-Groups-SHG-/assets/131864852/9e0e5efc-4f20-4dc3-914d-d03f5d6b908b)



Since I have calculated the total bookings, I want to get successful bookings. In the dataset, I have a column called canceled, where “0” represents successful bookings and “1” represents unsuccessful bookings. I will create a function that will count only the successful bookings. Using the count row Dax function.
Successful Bookings = CALCULATE (COUNTROWS ('Cleaned Data'),' Cleaned Data'[Cancelled (0/1)] = 0)

![image](https://github.com/Jawah1/Splendor-Hotel-Groups-SHG-/assets/131864852/bd3a8f4f-304f-4df7-91e1-9e686f8713c7)

 
Unsuccessful Bookings = CALCULATE (COUNTROWS ('Cleaned Data'),' Cleaned Data'[Cancelled (0/1)] = 1)

![image](https://github.com/Jawah1/Splendor-Hotel-Groups-SHG-/assets/131864852/a2f23644-d3e5-4309-946d-ec17b747ab45)

 
I then used the card visualization to get

1.	Total revenue
2.	Total guest
3.	Total Revenue lost

 ![image](https://github.com/Jawah1/Splendor-Hotel-Groups-SHG-/assets/131864852/21f7cc94-4b13-4b04-946f-c7ab948936f8)

 
The next thing I did was to use visualization to address some of the objectives.
First, I visualize the booking trend by month, average daily Rate by Distribution Channel, Cancelled by Customer Type, Countries with highest Revenue, Revenue by Distribution Channel.

Below is the dashboard Applied filters to drill down on each visualization on the dashboard.

![image](https://github.com/Jawah1/Splendor-Hotel-Groups-SHG-/assets/131864852/994a852e-ed56-44e7-80b4-574a75c37b15)

 

# Addressing Objectives and Recommendations

# Booking Patterns:

•	What is the trend in booking patterns over time, and are there specific seasons or months with increased booking activity?

•	How does lead time vary across different booking channels, and is there a correlation between lead time and customer type?

Answer and Recommendation

In terms of booking patterns, SHG had more bookings in 2016 compared to 2015, 2014, and 2017. While it did well in 2016, there was a drop in bookings in 2017. This is because of a decrease in bookings from online travel agents. Therefore, SHG should prioritize strengthening its relationship with online booking agents.
The first quarter has the highest number of bookings with January being the peak. These guests who book by this time check in between March to October. Since most bookings come in Q1, the business should increase its marking effort around Q3 of the previous year.

![image](https://github.com/Jawah1/Splendor-Hotel-Groups-SHG-/assets/131864852/0db1c5ac-6f52-4737-849e-1db9a68377bd)

 
# Customer Behavior Analysis:
•	Which distribution channels contribute the most to bookings, and how does the average daily rate (ADR) differ across these channels?

•	Can we identify any patterns in the distribution of guests based on their country of origin, and how does this impact revenue?

Answer and Recommendation

The distribution channel with the most bookings is the Online Travel Agent, it also has the highest average daily rate. As suggested earlier, the business should improve its relationship with online travel agents and, if possible and offer them incentives on bookings. The country with the most bookings and revenue is Portugal. Portugal. The least-performing country is Madagascar.


# Cancellation Analysis:
•	What factors are most strongly correlated with cancellations, and can we predict potential cancellations based on certain variables?

•	How does the revenue loss from cancellations compare across different customer segments and distribution channels?

Answer and Recommendation

There is a total of 44,000 canceled bookings against 75000 successful ones. The canceled booking is half that of the successful ones. This is not good at all. I recommend that the business request all guests to pay at least 45% of the room rate at the point of booking this will bring down the rate of canceled bookings.

# Revenue Optimization:

•	What is the overall revenue trend, and are there specific customer segments or countries contributing significantly to revenue?

•	Can we identify optimal pricing strategies based on the Average Daily Rate (ADR) for different customer types and distribution channels?

Answer and Recommendation
Portugal, the UK, France, Spain, and Germany contribute the highest revenue, this revenue is coming from transit customers. SHGs should target mostly transient customers in these countries.


# Comparison of Online and Offline Travel Agents:
•	What is the revenue contribution of online travel agents compared to offline travel agents?

•	How do cancellation rates and revenue vary between bookings made through online and offline travel agents?

Answer and Recommendation

Online travel agent brings in more revenue (17M) compared to offline travel agent that brings in just 7M.
Even though Online travel agent has more revenue, they still have more canceled bookings should strengthen their relationship with online travel agents and implement the 45% deposit on booking, which will close the gap in canceled bookings and revenue loss.

# Final Dashboard







