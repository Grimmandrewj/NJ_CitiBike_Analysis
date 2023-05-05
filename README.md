## Link to Tableau Public Page: 
https://public.tableau.com/app/profile/andrew.grimm4479/viz/CitiBikeViz_16830667040600/Analysis?publish=yes

## Goal
- For this challenge, I was tasked with generating reports for officials for the New York Citi Bike program in order to publicize and improve the program
- The premise was that the data has been regularly updated, but the team has yet to implement a dashboard or sophisticated reporting process for visualizing the data.  
- I was tasked with obtaining monthly datasets in the form of csv files from the Citibike data webpage: https://citibikenyc.com/system-data and review and visualize the data using Tableau

## Method
- For the challenge, I chose to download csv files for data between January 2020 and January 2021 (13 datasets total, located in Citibike Data folder in this github)
- I initially attempted to join all the datasets within Tableau, but discovered that due to their size and the number of records, Tableau was having trouble joining more than 5 datasets without locking up
- I therefore read in the csv files using Pandas and merged them into one combined dataframe.  This new dataframe was written out as a new csv file which included all the data
- From there, I explored the data using Tableau and searched for interesting phenomena to visualize in dashboards and a story page
- I discovered trends for the total number of trips logged and the percent change by month, numbers of users by usertype, peak hours in summer and winter months, etc.  

## Summary and Results
- The data demonstrated a total of 348,426 trips from January 2020 to January 2021.  The greatest change month to month was between April 2020 and May 2020, which showed a 170% increase in the amount of trips.  This was visualized using bar charts:

![image](https://user-images.githubusercontent.com/120341249/236355908-5e8fc2df-00f4-4a3c-bd3f-c7e619b0e72c.png)

- I visualized the top ten busiest stations for beginning trips, and the bottom ten stations for ending trips.  This data was visualized with bar charts and interactive maps.  The starting station with the highest number of trips was Groven St PATH, and the bottom station was JCBS Depot: 

![image](https://user-images.githubusercontent.com/120341249/236356279-38147d59-4c61-4ffe-a575-5581a83c1dca.png)

- Using line charts, I also visualized the number of Customers (casual users) and Subscribers over the course of this dataset.  I also visualized the number of usertypes by gender.  Customers rose sharply from April 2020 to June 2020, but dropped thereafter.  Subscribers rose sharply from April 2020 to October 2020 and then fell sharply.  The "unknown" gender selection represents the majority of Customers, while male users reflect the highest number of Subscribers: 

![image](https://user-images.githubusercontent.com/120341249/236356540-2bd522f1-0915-4399-86e7-56b5c2ac550e.png)

- Using bar charts, I visualized the peak hours for trips in the Summer and Winter months. In the summer months, trips peaked between 5-7 pm, while in the winter, they picked at 8 am and again at 5-6 pm.  Overall trips in the winter months were around half of the total in the summer months: 

![image](https://user-images.githubusercontent.com/120341249/236356873-f93602bd-dab7-4ce7-be2c-371439e65c68.png)

- Using a line, bar, and pie chart, I then visualized the amount of gender users by date of birth and age, the total users by gender, and the percentage of users by age and gender.  The highest age logged by users was 133 years (year of birth 1888).  There are also several other listings with an age over 90, which I feel is likely incorrect/false data.  These were marked as outliers in the legend.  A high number of users (51k+) also listed their year of birth as 1969, which is far higher than the number of any other year of birth.  I also feel this likely represents possible false data or a "place holder" used by the majority of users.  Male users represent the majority of overall users (nearly 60%): 

![image](https://user-images.githubusercontent.com/120341249/236356935-b7c42a80-e12c-423b-b664-9b2cc7908bb5.png)

- Finally, using bar charts, I visualized the average trip duration by station as well as the most used bikes by Bike ID.  Users beggining their trip at the Union Street station logged the longest average trip duration by a significant amount more than the next highest (4600 vs. 3000 for the next station).  Bike IDs 44683 and 40831 logged the longest distance overall by a wide margin compared to the other Bike IDs.  They vast majority of users of these two bikes were also Subscribers:

![image](https://user-images.githubusercontent.com/120341249/236357183-e8c49c78-d9f8-4667-b4da-426e7409a8a8.png)



