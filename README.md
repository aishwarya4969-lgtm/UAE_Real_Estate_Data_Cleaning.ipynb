# UAE_Real_Estate_Data_Cleaning.ipynb

I took a raw web-scraped dataset of 41,381 Dubai listings and built a Python cleaning pipeline using Pandas to strip out the noise and deliver an accurate dataset ready for market analysis.

The Stack  Python & Pandas for the heavy lifting 
Google Colab as my development workbench

The Real Impact

Starting Point: 41,381 messy listings
Final Count: 14,389 clean, unique properties

The Clean-up: I wiped out 26,992 junk records (a huge 65.2% reduction in data clutter) so any future dashboard averages are completely accurate.

What I Actually Fixed

1. Nuking the Broker Duplicates - There weren't many 100% exact matching rows because of different scraping timestamps, but the property data itself was massively repeated. I ran a smart check to find rows where price, property type, beds, and baths matched perfectly.

The Fix: Caught and dropped 26,968 overlapping broker listings, saving only the very first original post.

2.Hunting Down Price Errors - Properties in Dubai obviously aren't free. My initial audit flagged a few listings with a price tag of exactly 0 AED.

The Fix: Dropped those 8 broken records. This fixed my averages and set a clean, realistic market baseline price of 95,000 AED.

3. Fixing Map Coordinates - You can't build a real estate map chart if your coordinates are blank. I scanned for missing locations.

The Fix: Removed 16 rows missing Latitude or Longitude. Since it was under 0.1% of the total dataset, dropping them kept the mapping visuals airtight without hurting our data size.

The Deliverable - I exported everything into cleaned_uae_properties.csv. It’s fully optimized and ready to plug straight into Power BI or Tableau for interactive neighborhood pricing maps without breaking any charts.
