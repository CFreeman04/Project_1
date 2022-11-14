# Project_1
EDA &amp; Git Collaboration
#Christian Nava - Clean Data

Remove missing data
    N/A's removed using .dropna()
       Rows with N/A's were exclusively present in all measured columns
       487 rows with N/As present out of 318,016 rows of data, leading to the conclusion that a neglegable number of rows can be deleted to eliminate N/A's and clean the data
Check for duplicate values
    Rows with duplicate values indentified using .duplicated()
        No duplicate rows identified after N/A's were deleted
Changed data type using .astype()
        Float64 values had to be changed to int values to manipulate with mathmatical functions
        
Determine busiest airports, or those with the most arriving flights from 2003 to 2021
    Arriving flights by airport name determined by using .groupby("airport_name") and placing this into a new dataframe
    New dataframe then sorted using .sort_values("arriving_flights") with ascending = False
        Atlanta, GA: Hartsfield-Jackson Atlanta International has the largest number of arriving flights, which may later lend itself to the largest number of delays, cancellations, and many other cumulative metrics due to the large number of overall traffic.

#Charlie Freeman

Find Carrier with most cancellations within a given month
    Used .max() against "Arrival Cancelled" column
        Delta Airlines had 4951 cancellations in March 2020
            Given the sudden onset of COVID incidents in the United States in March 2020, followed by lockdowns in April 2020, it can be concluded that COVID caused unusually large onset of cancellations for Delta Airlines in March 2020.
            This can be further visualized given the line plot of cancellations over time, greatly spiking over all carriers in March 2020.
            
Calculate the most delays within a given month
    Used .max() against "Delays" column
        Delta Airlines had 6377 delays in July 2005
        Delays across all carries were plotted against time in a line plot
            Looking at a plot of delays there appears to be a wave like pattern over the 18 years of data but drastic increases and decreases month over month. July 2005 had the largest number of delays.
            No direct correlation to newsworthy events could be found to explain the large number of delays in July 2005.
            There appears to be a markedly low amount of delays in March, April, May of 2020. This is actually due to the low amount of overall flights during that time due to COVID lockdowns.
            
            
After looking at available metrics of flights, locations, carriers, delays, cancellations, and all over time we see a significant impact of COVID-19 in the form of acute increase in cancellations followed by a temporary decrease in overall flights across the board. It is apparent that cancellations reached an all time high in March 2020 due to COVID, travel restrictions, and health concerns of the public. Delta Airlines seems to have been the most affected, choosing to cancel over 4900 flights. Flights were cancelled en masse at the onset of hysteria and lockdowns and new bookings/available flights were low in volume for several months to follow. For this reason we see an acute increase in cancellations that goes back down after a couple of months because there are less flights to be cancelled. This overall decrease in flights caused delays to sharply decrease around this same time as less flights are delayed if less flights are occurring. When looking at the largest number of delays in these 18 years of data, we see that the largest number of delays was also by Delta Airlines but on July of 2005. This is not due to COVID or known disease concerns. There is not an obvious news worthy event to tie to this increase in delays. When looking at the trend of delays a wave pattern is noticed with sharp increases and decreases month over month. for this reason there are many coparable moments in time with highest and lowest volume of delays. Both the largest number of delays and largest number of cancellation of arrivals 2003-2021 occurred at the same airport, Chicago, IL: Chicago O'Hare International. When looking at the heirarchy of arriving flights over all 18 years by airport name, Hartsfield-Jackson Atlanta International Airport has the largest number of overall arriving flights followed by Chicago, IL: Chicago O'Hare International. This leads to the conclusion that the airport's large volume of cancellations and delays are directly correlated to the large volume of arriving flights. However, Atlanta, GA managed to sustain less delays and cancellations with more overall arrivals.

