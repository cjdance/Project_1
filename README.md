# Project_1 - Melbourne Airbnb - 2019 vs 2020 - Impact of Covid-19
### Group repository for project in Monash Data Bootcamp

# Project Description

Our project aimed to look at available data for Melbourne AirBnB listings across 2019 and 2020 to identify trends in availability, room types offered and whether price or other factors affect bookings and review score.

### Data Sources
There were two datasets used for this project:
https://www.kaggle.com/tylerx/melbourne-airbnb-open-data
  * This dataset was compiled from the inside the AirBnB website on 7 December 2018
  * It shows all active listings for AirBnB and the next 12 months of their calendar (i.e. availability in 2019 for the properties)
  * It also contains a range of summary data and other information about the host
https://www.kaggle.com/nadyafed/melbourne-airbnb-2020
  * This dataset was also compiled from inside the AirBnB website, this dataset was created on 20 August 2020

We used the Listings dataset and Calendar dataset for both 2019 and 2020 to perform our analysis and generate output. All data was loaded and stored as CSV files.
Once the data was read, the data was manipulated to perform the analysis.

The outputs include a range of summary statistics, bar charts, boxplots, scatter plots and heat maps.

### Dataset Limitations

* Price in the 2020 dataset has the $ symbol - it was cleansed and formatted to remove the $ symbol using Regex and converted to float. 
* Availability is given as a True/False in the AirBnB calendar. We have assumed 'False' to be a booking.
* Pricing data presents extreme outliers within the dataset. This has been included in the data analysis. 
* Some of the data in the fields like suburb and amenities are manually entered by the hosts and has data discrepancies and inconsistencies.

### Insights from the Data

From the data, below are some of the conclusions we could draw

## Melbourne suburb with the most listings on AirBnB

The Melbourne AirBnB overall listings have decreased in 2020 by almost 10%. The top 5 Melbourne suburbs with listings in 2019 are as shown below. We can see that the same 5 suburbs have the most listings in 2020, however the numbers have decreased in 2020.
The change in listings have also been highlighted in the table below.

```
	   2019 Listings	2020 Listings	Change in Listings
Melbourne	7368	            6174	-1194
Port Phillip	2808	            2498	-310
Yarra	        2049	            1578	-471
Stonnington	1621	            1369	-252
Moreland	967	             863	-104	
```

## Melbourne suburb with maximum average days booked

The average and median days booked was calculated and below are the top 5 suburbs with most bookings in 2019 and 2020.
The top 5 booked suburbs were further analysed to look for trends during the busy months.

```
	city	   Average Days Booked 2019	Median Days Booked 2019   Average Days Booked 2020	  Median Days Booked 2020
0	Moreland	265.5149                           320.0	          252.209733	                           287.0
1	Yarra	        265.232796	                   327.0	          253.365019	                           341.0
2	Darebin	        259.992837	                   323.0	          256.111111	                           333.0
3	Melbourne	242.376629	                   289.0	          231.425656	                           275.0
4	Stonnington	239.495373	                   294.0	          235.598977	                           278.0
```

## Number of room types in 2019 and 2020

We found that the Airbnb Room types were categorised as 'Entire home/apt', 'Private Room' and 'Shared room' in 2019. A new listing 'Hotel Room' was introdced in 2020. 
The number of listings under each room type have decreased in 2020 compared to 2019 as can be seen below

```
                room_type	listing_id
0	      Entire home/apt	14379
3	      Hotel Room	0
1	      Private room	8116
2	      Shared room	400
```
```
               room_type	listing_id
0	     Entire home/apt	12613
1	     Hotel room	        227
2	     Private room	7161
3	     Shared room	419
```

## Average number of days booked for room types in 2019 and 2020

We found that the average number of days booked have increased in 2020 for entire home/ apartment and private rooms. The average number of days booked in Shared rooms have decreased in 2020.
```
              listing_id	Number of Days Booked	Price per Night
room_type			
Shared room	2.920812e+07	    267.890141	            54.963380
Private room	2.637645e+07	    256.258458	            87.843128
Entire home/apt	2.584060e+07	    229.238128	           184.287671
Hotel room	2.890528e+07	    181.909091	           215.285000
```

## Median Price of room types 
It was found that the median price of room types slightly increased or remained the same in 2020 compared to 2019. We can also see the median price increase for some of the regional suburbs in 2020 compared to 2019.

## Correlation between Review Score Rating and Price per Night
Plotted a scatter plot to check for any correlation between review score and price. There is only weak correlation between Review rating and Price per Night of a listing in AirBnB. The r-value was found to be 0.04 for 2019 and 0.03 for 2020.

## Correlation between Number of days booked and Price per Night
Plotted a scatter plot to check for any correlation between number of days booked and price. There is only weak correlation between Price per Night and Number of days booked for a listing in AirBnB. The r-value was found to be -0.11 for 2019 and -0.04 for 2020.

## Correlation between Host response and Number of days booked
Plotted a scatter plot to check for any correlation between number of days booked and host response. There is moderate correlation between Host Response Rate and Number of Days booked for a listing in AirBnB. The r-value was found to be -0.34 for 2019 and -0.4 for 2020.


### Guide to Repository

You can find the code in the Jupyter Notebook file called "airbnb_final.ipynb".

The folder named "output files" contains the output plots generated.

This ReadMe file contains the description of the homework, data limitations and snippet of some of the data statistics.


