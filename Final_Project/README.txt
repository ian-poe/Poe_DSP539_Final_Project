This Project uses R 4.2.3 

This Folder contains five items including data sets, r-markdown code, and a pdf report of this project.
The following will go through each of these five items to make the understanding and running project easier.

The Project: Ground Fish Analysis around Deepwater Horizen Oil Spill



Data: 
    There are three publicly avalible datasets used in this analysis. 
    One dataset belongs to a trawling datset in the Gulf of Mexico,
    While the other belong to a long-line dataset.

DWH Baseline SEAMAP Groundfish.csv:
  This Data is a copy of the public data from NOAA which can be found at this Link: https://www.fisheries.noaa.gov/inport/item/32334
  The website provide a indepth description of the data along with the variables withing the dataset.
  This Trawling Dataset which collected data from 1987 to 2010 and will be the first used in the analysis.

catch.csv:
  This Data is a copy of the public data from NOAA which can be found at this Link: https://www.fisheries.noaa.gov/inport/item/31654
  The website provide a indepth description of the data along with the variables withing the dataset.
  This is one of multiple dataset related to the long-line datasets (to see the other datasets go to the link above)
  For this project is the first of the two long-line datasets used for the analysis
  This Long-line Catch Dataset shows the catch data from 1995 to 2013.

station.csv:
  This Data is a copy of the public data from NOAA which can be found at this Link: https://www.fisheries.noaa.gov/inport/item/31659
  The website provide a indepth description of the data along with the variables withing the dataset.
  This is one of multiple dataset related to the long-line datasets (to see the other datasets go to the link above)
  For this project is the second of the two long-line datasets used for the analysis
  This Long-line Catch Dataset shows the catch data from 1995 to 2013.



The Report:

Poe_DSP539_Final_Project.pdf: 
  This pdf document is the Final Report of the "Ground Fish Analysis around Deepwater Horizen Oil Spill".
  Within this document you will find the most relevent figure, statistics, and analysis which whereused in order to answer    the four main questions in the report.
  Question 1: Using Bottom Trawling Data, is Marine Life Affected by the Oil Spill?
  Question 2: Are we Able to Compare the Data from 2010 to the Data of Other Years?
  Question 3: Using the Bottom Trawling Dataset as a Baseline; Can We Identify Species of
  Interest and Apply it to the Long-line Fishery Dataset?
  Question 4: Using Long-line Data From after the Oil Spill Can Any Conclusions be made
  From That the spill affected Benthic Marine Biology
  The Figures and the conclusions can be found in this document



The R-Markdown Code: (Using r 4.2.3)

Poe_DSP539_Final_Project.Rmd:
    This R-markdown file contains all of the code to create the figures from the report.
    In addition to the signficant figures included in the report additional figures, dataframes, and list can be found.
    The r-mardown is broken down by question and commeted to allow easy understanding of what is occuring.
    Before running the code ensure all of the library specified at the top of the code is downloaded to your r-studio.
    Lines 26, 410, and 411 are where the datasets located above are imported into the data. 
    Depending on the saved location for these data sets the path may have to be changed. 
    
    This code contains the following 5 functions:
    
    make_series(df, value_col, type_label, year_label):
        This uses a dataset and a specified value column to create a dataframe of mean of the value_col for each day of a specified year.
    location_per_year(data,year):
        This creates a map of the gulf of mexico with all the trawling location for the year plotted
    depth_per_year_density (data, year1, year2):
        This creates overlaying density plots to see how the density of the depth variable changes from year1 to year2
    speed_per_year_density(data, year1, year2):
        This creates overlaying density plots to see how the density of the speed variable changes from year1 to year2
    Species_Greatest_Change(data, ref_year, n):
        This finds the species of intrest from the trawling dataset.
        By providing a reference year the diffrence from the referance year to 2009 is found and
        the top n species with the greatest positive and the top n species with the greatest decrease are identified 

    The code also shows how all of the data is analyzed and how all of the figures are created. 


    **FOR A MORE DETAILED UNDERSTANDING OF THE CODE SEE THE COMMENTS IN THE FILE**
