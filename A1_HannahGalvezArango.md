CEE 224X | Released: 180925 | Due: 181002
Name: Hannah Galvez-Arango

#### Q1: What are the “Combined” fields referring to? How do you think this information may affect our analyses?

The "Combined" field lists whether or not a particular data entry is an aggregation of multiple neighboring zip codes' data or not.  According to the PG&E website, the California Public Utilities Commission requires that publicly available energy usage data only be published for individual zip codes if there are certain numbers of residential and non-residential customers present.  Zip codes that do not reach this minimum have their data combined with an adjacent zip code to protect the anonymity of customers.  This could make it seem as if sparsely populated areas use more energy than they actually do, skewing our data towards higher energy usages.



#### Q2: Why are the “Average” fields likely not useful for our analyses?

The "Average" field does not allow for any meaningful comparison between electricity and gas consumption because the data is in different units of measurement that are not easily converted.  For electricity consumption, the values in "Average" are in the form kWh/customer, while the gas values are in the form therms/customer.  It is easier to convert the electricity and gas totals to kBTU, then calculate an average or compare totals or averages in a chart.  



#### Q4: What is the total KBTU combined electricity and gas consumption in PG&E territory in 2017? What is the average annual electricity consumption per customer, and average annual gas consumption per customer?

The total combined electricity and gas consumption in PG&E territory was 2.89205E+11 kBTU in 2017.  The average annual electricity consumption per customer was 1838.025398 kBTU, and the average annual gas consumption per customer was 3457.03372 kBTU.  



#### Q5: How would you explain the results of this chart to an average property owner in Northern California? What would be the value of conducting further "seasonal" analyses of energy use, compared to "year-long" analyses, and how would you define seasonal boundaries?

This chart shows monthly fluctuations in the total energy usage of all PG&E customers.  By comparing electricity and gas usage, we can see that electricity consumption is generally lower and more consistent than that of gas.  Electricity usage is the highest in summer, probably because people are using their air conditioners, while gas usage is highest in the winter because people are using gas-powered heaters.  Seasonal analyses might help reveal more subtle trends in energy usage unrelated to home temperature control.  Seasonal boundaries could be defined by simple groupings of three months (Jan-Feb-March, and so on) or by average temperature cutoffs (ex: 9/21-12/21 yielded a certain average high and low temperature).  The former would be easier to implement, but the latter would produce a more accurate grouping of seasons.  If I had a decent amount of time, I would use the average temperature bounds to define the seasons.  



#### Q6: Explain your choice of formula for "avgkbtu".

I used =IF(Dx,Bx/Dx,0) to generate my entire "avgkbtu" column where x is the corresponding row number.  In this formula, the B value was total energy consumed in kBTU, and the D value was total customers.  I used an IF statement that I read about in Excel Help in order to avoid generating #DIV/0! errors.  Adding the IF portion effectively told Excel to list a 0 for any calculation where the denominator (number of customers) would be zero.



#### Q7 Paste a publicly viewable link to your Slides.

https://docs.google.com/presentation/d/1mAYLf2XZGFFt2mcNWNkG2FnI8XMuygi1jQdhInqXyUc/edit?usp=sharing



#### Q8 In what ways do the results in or in the vicinity of your chosen zip code validate or contradict your expectations?

I expected the total energy consumption of the Visalia area to be relatively low, and it was.  Visalia is located in rural Tulare County, where population density is much lower than the coastal metropolitan regions of California, so it follows that the area would use less energy overall.  However, I thought the area's average energy usage might be in the moderate range because people may heat their homes during the winter.  The low average energy usage may be due to economic factors.  According to the 2017 American Community Survey, nearly 50% of Tulare County households had an income of less than $50,000, so many residents may not be able to afford energy-intensive appliances.  



#### Q9 Any other reactions to completing Pass One? What was especially challenging or surprising in the workflow? How might you expand on this analysis if you had more time?

The Excel portion took longer than I expected and helped me realize that I still have a lot to learn about Excel.  Finding the "IF" formula I used in question 6 led me to realize that some of the logical statements I have learned through GIS software and R can be applied to Excel as well, which will be very useful.  The ArcGIS portions were very familiar, but I did have some interesting temporary glitches that all resolved when I exited and restarted the program.  (I completed this assignment in a slightly older version of ArcGIS, but I will update it for the next assignment.)  I would expand on this analysis by running Moran's I and Getis-ord GI* analyses to locate clusters of low and high energy usage.  It might also be useful to add another layer depicting major cities to the maps so we could visually compare energy usage and population.  



#### Q10 How would you compare the experienced or apparent work involved, as well as the usefulness of the outcome, of Pass One vs. Pass Two? How would you rate the difficulty of this assignment?

Pass Two was particularly cumbersome for me because I had a bunch of technical issues with my computer (antivirus blocking my R packages, etc).  Fixing those issues took so long that I didn't spend as much time examining the code and learning from it as I would have like to.  Part Two helped dust off the cobwebs on some aspects of R for me, but it also reminded me of how much I don't know about R.  I prefer Pass One because I like working with ArcGIS more and can readily access more aesthetic and analytical tools through ArcMap.  This assignment felt reasonably difficult.  It would be great if there could be a more challenging optional ArcGIS portion.  Like the coding portion, there could be a short set of tasks to perform listed before the detailed instructions so more experienced GISers could try to figure those parts out by themselves.  



#### Q11 In total, how long did Assignment 1 take?

Part 1: Tech Setup: 90 minutes

Part 2: Pre-Assessment: 15 minutes

Part 3: Readings: 0 minutes (I don't think there were any readings.)

Part 4: Practice Data Dive: Pass 1: 150 minutes (I had to redo some steps because I accidentally converted to BTU, not kBTU, at first.)

Part 4: Practice Data Dive: Pass 2: 120 minutes
