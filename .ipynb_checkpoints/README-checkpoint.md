# Pink Buckle Project

## Installation
 
 This analysis is of the Pink Buckle Barrel Racing Futurity for 2018-2020. 
 
Results were taken from https://www.pinkbuckle.com/race-results/ in pdf form and converted to a csv file with the Tabula package for Pandas. 
 
I have converted the PDF Files to CSV which can be found here.  To replicate that process: Tabula can be accessed here https://tabula-py.readthedocs.io/en/latest/


 
## Project Motivation

This project was undertaken for a Udacity Nano-Degree Program. I chose to utilize the pink buckle results because it was of personal interest to me at the time. 
 
Formatting for the results varied from year to year. The manipulation of the data into a clean dataframe was done in a script that is quite crude. Steps are similar from year to year and some columns were dropped prior to creating the final CSV.   
 
Money winnings did not come through readily with Tabula and I did not put much effort into bringing in the dollar amounts, only assigning a value to those. My analysis focused on the stallions. The goal was to determine which stallions had the highest percentages of money winners, offspring placing in the top division and most entries.
 

  
  
### Business Understanding/Data Understanding

Barrel Racing has become big business in the equine industry.  Winning horses are often selling in the range of the upper five figures to lower six figures. As this sport has grown and matured, new events are being created to showcase these athletes beyond the rodeo arena.   

One such event is the Pink Buckle barrel race.   According to their website, “It is designed to dramatically increase the number and quality of barrel racing performance horses by promoting the Pink Buckle stallions and their offspring. The Pink Buckle had its first race in 2018 and its popularity has skyrocketed. With $2.7 million in prize money for 2021 - it’s a very lucrative competition for the winners. However the Pink Buckle race is a very exclusive event . Only sons and daughter of 50 individual stallions are eligible. Horses that are eligible to run in this particular futurity are in high demand and accordingly, command a higher price tag. 

I was considering out-crossing a cutting bred mare to a barrel racing sire. Pink Buckle Eligible foals are in demand. I had an intuitive understanding of the results because I've grown up around the events, and had several friends with horses running in the futurity.  

### Data Prep

The data set I utilized were PDFs available from PinkBuckle.com of past futurity race results.  Files were converted from PDF and analyzed using Pandas.

Conversion from PDF did not read in the entirity of the results - payouts were left out.  I chose not to brute force the information into my analysis as it would not scale to a larger analysis.  There were a number of anomalies with spelling errors, and formatting.   Result formats varied from year to year and required a separate methodology to create a tidy version of the data with one  piece of data in each column. 

The 3 years of results were concatenated into one dataframe for analysis.  

Results reported any penaly during the run as a 999.00 second time.  Many races report penalties as a time and a number of penalties. Unfortunately I had to exclude the no times from any calcuations of averages by changing them to a NAN.  I did preserve a count of penalties by horse.  

### Model Data

The data was grouped by sire. From that I created an average time of all offspring, excluding penalty times, for each sire.  

There were not enough horses to in the dataset to have meaningful results from any type of machine learning.  Instead I calculated statistics on the sires based on their offspring's perfomance.   Average time,  number of horses placing in the first division, how  many of each stallions offspring won money based on the 2020 payout system were all calculated values.

I used the calculated statistics to look at correlations of stud fee to offspring performance.  

One Famous Eagle has more offspring competing on the track, sucessfully, than barrel racing.  His stud fee was reported as private treaty.  I generally assume private treaty means if you have to ask, you can't afford it.  Online forum rumors suggest that the number is over $12k, but I did not include him inany calculations. 

### Results
The findings from my analysis confirmed some of my hunches from looking at the results, but surprised me in many ways.  The analysis really emphasized the sucess of the stallion Streakin Boon Dox.

I set out to answer the below questions.  For visuals please see my medium post or review the notebook PBLab.ipyb
#### Which stallions had the most offspring entered?
Slick By Design was the most prolific sire. 


#### Which stallions’ offspring produced the most horses who placed in the 1D?
The Goodbye Lane — 66.7%

#### Who’s offspring had the best average time for the futurity?

Dats a Frenchman — 35.388 Seconds

#### Which stallion sired the most money winners?
Carrizzo — 50%
Streakin Boon Dox — 50%


#### Is there any connection between performance and Stud Fee?

I there is a slight correlation between stud fee, percentage of money winners and and placing in the 1D.  But I do not consider the values to be a strong correlation.  

for a more through discussion of how my analysis relates to barrel racing, and graphs please visit my medium artice: 
https://baileyee.medium.com/which-pink-buckle-futurity-stallion-is-most-likely-to-produce-a-winner-64b212877477

## Deploy

My information was utilized to inform several mare owners of the perfomance of pink buckle stallions.  

The code in this notebook could be utilized to expand analysis to another futurity/race the Ruby buckle which contains all pink buckle sires and 50 additional.  It would also be interesting to see if there is any correlation between sucessful horses and the a cross of daughters of a particular stallion on the individual studs in the analysis.  

Expanding the analysis to include the open races could also provide additional insight if the medium article generates any interest. 

##  File  Description

### PDFResults_to_CSV.ipynb

 the conversion from PDF to a messy CSV format.  Conversion utilized the tabula-py
 Tabula can be accessed here https://tabula-py.readthedocs.io/en/latest/


### SireFees.ipynb

contains information on the 2021 Pink Buckle Stallions scraped  Feb 3 from https://www.qstallions.com/StallionDir?id=Speed%20Events&w=2&PB=1
It also was used to create a plot of stud fee frequency.  This data was later used in PBLab. 

### Files folder
contains the PDFs of all Pink Buckle Futurity results from 2018-2020, including a roster of all pink buckle stallions during the lifetime of the event.  

### CSV_Year_results Folder
contains the CSV files created by PDFResults_to_CSV

### CSV_Analysis Folder

Contains CSV files created during the analysis. 

##  Aknowledgements

I'm incredibly grateful to Dr. Shannon Neegard-Paper for her encouragement to pursue this project and keep forging ahead in my setbacks.  She was also of tremendous assistance in pointing me toward resources that helped push through the project. 

My Husband has been accomodating in watching our twin 18 month olds and picking up the slack at home while I "just need to finish one more thing".  

I also appreciate the Pink Buckle futurity for providing results from their events to the general public.  I had asked if they would provide the original excel files, but was told no.   Converting files from PDF and working with the Data has been a fabulous learning experience for a PANDAS rookie.  

Q stallions online provided some fabulous insights and provided an easy source of 2021 stud fees, rather than visiting each stallions website or facebook page.  