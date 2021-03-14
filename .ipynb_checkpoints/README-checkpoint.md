# Pink Buckle Project
 This analysis is of the Pink Buckle Barrel Racing Futurity for 2018-2020. Results were taken from https://www.pinkbuckle.com/race-results/ in pdf form and converted to a csv file with the Tabula package for Pandas.  
 
 Formatting for the results varied from year to year. The manipulation of the data into a clean dataframe was done in a script that is quite crude. Steps are similar from year to year and some columns were dropped prior to creating the final CSV.   
 
Money winnings did not come through readily with Tabula and I did not put much effort into bringing in the dollar amounts, only assigning a value to those. My analysis focused on the stallions. The goal was to determine which stallions had the highest percentages of money winners, offspring placing in the top division and most entries.
 
This project was undertaken for a Udacity Nano-Degree Program. I chose to utilize the pink buckle results because it was of personal interest to me at the time. The Analysis followed the CRISP-DM process. 
  
  
## Business Understanding/Data Understanding

Barrel Racing has become big business in the equine industry.  Winning horses are often selling in the range of the upper five figures to lower six figures. As this sport has grown and matured, new events are being created to showcase these athletes beyond the rodeo arena.   

One such event is the Pink Buckle barrel race.   According to their website, “It is designed to dramatically increase the number and quality of barrel racing performance horses by promoting the Pink Buckle stallions and their offspring. The Pink Buckle had its first race in 2018 and its popularity has skyrocketed. With $2.7 million in prize money for 2021 - it’s a very lucrative competition for the winners. However the Pink Buckle race is a very exclusive event . Only sons and daughter of 50 individual stallions are eligible. Horses that are eligible to run in this particular futurity are in high demand and accordingly, command a higher price tag. 

I was considering out-crossing a cutting bred mare to a barrel racing sire. Pink Buckle Eligible foals are in demand. I had an intuitive understanding of the results because I've grown up around the events, and had several friends with horses running in the futurity.  

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

