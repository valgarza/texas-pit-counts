# README
The dataset includes data from Point-In-Time counts performed across five different continuums of care (CoC) in Texas. The intended audience is activists and researchers looking to standardize data on homeless across counties and cities.

This README file will contain information on the dataset, including a data dictionary, metadata, and information on naming conventions and data normalization. 

The data is available in a .csv.

## Table of Contents

1. Naming Conventions
2. Data Normalization
3. Data Dictionary
4. Metadata
5. Security
6. Contact

## Naming Conventions

Files are named for maximum clarity. The following format should be used:

> *dyear*_pitcounts_*datatype*

As this dataset only contains data from 2020, that is all that will be available. There are two types of data aggregated for each year: *summary* and *demographics*. Thus there are two .csv files for 2020 for each type. 

## Data Normalization

Most of the data collected was transcribed as was printed in the original reports. However, at times certain figures needed to be added together, or percentages ennumerated, in order to provide accurate figures within the dataset. All values derived from this method were rounded to the nearest whole number and cross-referenced with the totals provided, in order to remain accurate (also, 0.243ths of a person can't actually exist, errors like that are mostly due to imprecise reporting in the PIT count reports). 

## Data Dictionary

| Variable | Variable Name | File | Measurement Unit | Allowed Values | Definition |
| --- | --- | --- | --- | --- | --- |
| regionName | Name of region | both | string | US State/County Name/s | The name of the county or CoC |
| population | Population | summary | integer | Integers greater than 0 | The total population for a given region. If multiple counties are counted within a region, the population totals of each county were added together. |
| sheltered | Sheltered Homeless Population | summary | integer | Integers greater than 0 | The total number of sheltered homeless people. Counts that distinguished between Emergency Shelter and Transitional Shelter were added together. |
| unsheltered | Unsheltered Homeless Population | summary | integer | Integers greater than 0 | The total number of unsheltered homeless people. |
| homelessTotal | Total Number of Homeless People | both | integer | Integers greater than 0 | The total number of homeless people, sheltered or unsheltered. |
| hhwc | Households With Children | summary | integer | Integers greater than 0 | The total number of households with children. Households are a common statistic found in PIT counts. |
| hhwoc | Households Without Children | summary | integer | Integers greater than 0 | The total number of households without children. | 
| childrenOnly | Households with Only Children, Unaccompanied Youth Households, & Parenting Youth Households | populationTotals | integer | Integers greater than 0 | The total number of households with only children, unaccompanied youth households, and parenting youth households. The previous three categories are sometimes but not always differentiated in PIT counts, and if they, the latter two are counted separately from only-children households. If this was found to be the case, the totals from each were added together. |
| householdsTotal | Total Number of Households | summary | integer | Integers greater than 0 | The total number of homeless households. Usually the sum of the three previous variables, but if unaccompanied youth households and parenting youth households were counted separately, the figure would be adjusted to account for their reporting. |
| volunteers | Number of Volunteers | summary | integer | Integers greater than 0 | The number of volunteers reported to have conducted the count. |
| surveysTotal | Total Number of Surveys Conducted | summary | integer | Integers greater than 0 | The total number of surveys conducted by volunteers during the PIT count. This is in contrast to observation-only counting, and is how the majority of demographic data is collected: through self-reporting by homeless individuals. |
| age_under18 | Number of Homeless Youth | demographics | integer | Integers greater than 0 | The total number of homeless children under the age of 18. The first of three age categories found in every PIT count. | 
| age_18to24 | Number of Homeless Young Adults | demographics | integer | Integers greater than 0 | The total number of homeless young adults between the ages of 18 and 24. The second of three age categories found in every PIT count. | 
| age_over24 | Number of Homeless Adults | demographics | integer | Integers greater than 0 | The total number of homeless adults over the age of 24. The third of three age categories found in every PIT count. |
| race_white | Number of White Homeless People | demographics | integer | Integers greater than 0 | The total number of homeless people who self-identified as White. Usually expressed as a percentage of the total number of homeless people, so a conversion from percentage to a whole number was necessary. This is true of every race category that follows. | 
| race_black | Number of Black Homeless People | demographics | integer | Integers greater than 0 | The total number of homeless people who self-identified as Black. | 
| race_asian | Number of Asian Homeless People | demographics | integer | Integers greater than 0 | The total number of homeless people who self-idenfitied as Asian. | 
| race_AIAN | Number of American Indian and/or Alaska Native Homeless People | demographics | integer | Integers greater than 0 | The total number of homeless people who self-identified as American Indian and/or Alaska Native. | 
| race_pacificIslander | Number of Hawaiian Native and/or Pacific Islander Homeless People | demographics | integer | Integers greater than 0 | The total number of homeless people who self-idenfitied as a Hawaiian Native and/or a Pacific Islander.  In the instance that AIAN and Pacific Islander statistics were grouped together, this cell was marked null. |
| race_otherMult | Number of Homeless People reporting Other/Multiple Race(s) | demographics | integer | Integers greater than 0 | The total number of homeless people who identified outside the prescribed categories, or identified as multiracial. | 
| ethnicity_His | Number of Hispanic/Latinx Homeless People | demographics | integer | Integers greater than 0 | The total number of homeless people who identified as ethnically Hispanic/Latinx. These were the only available ethnicity categories, and were usually marked alongside race. | 
| ethnicity_nonHis | Number of non-Hispanic/Latinx Homeless People | demographics | integer | Integers greater than 0 | The total number of homeless people who did not identify as Hispanic/Latinx. If only the previous statistic was recorded, this cell was marked null. | 
| gender_male | Number of Male Homeless People | demographics | integer | Integers greater than 0 | The total number of self-idenfitied "male" homeless people. | 
| gender_female | Number of Female Homeless People | demographics | integer | Integers greater than 0 | The total number of self-idenfitied "female" homeless people. | 
| gender_trans | Number of Transgender/Gender-Nonconforming Homeless People | demographics | integer | Integers greater than 0 | The total number self-identified as "transgender" or "gender-nonconforming". If the two were marked as separate figures, they were added together for this dataset. |
| veteranStatus | Number of Homeless Veterans | demographics | integer | Integers greater than 0 | The number of homeless veterans who self-reported. Data for veterans was often reported alongside other demographic information, but not always. | 

## Metadata

| Attribute | Value |
| --- | --- | 
| title | Texas PIT Counts by Region (2020) | 
| description | The dataset includes data from Point-In-Time counts performed across five different continuums of care (CoC) in Texas. The intended audience is activists and researchers looking to standardize data on homeless across counties and cities. |
| keyword | “Texas”, “Travis County”, “Cameron County”, “Harris County”, “Fort Bend County”, “Montgomery County”, “Bexar County”, “Homelessness”, “Point in Time”, “pit”, “count”, “HUD” | 
| modified | 2023-03-10 | 
| publisher | Valentine Garza, University of Washington Seattle | 
| contactPoint | Valentine Garza valgarza@uw.edu | 
| described by | --- | 
| accessURL | --- |
| downloadURL | --- |
| language | en-us | 
| rights | This data is freely available to the public. | 
| references | https://www.thn.org/wp-content/uploads/2020/07/Final-Combined-Report-1.pdf, https://www.census.gov/quickfacts/fact/table/US/PST045222, https://www.thn.org/wp-content/uploads/2020/03/Cameron-County-Homeless-Coalition.pdf, https://www.sarahomeless.org/uploads/1/4/0/6/140635251/pit-2020-final-pdf.pdf, https://www.austinecho.org/wp-content/uploads/2020/10/PIT-2020-Source-Document.-Revised-to-correct-Table-4-and-Figure-13.10.21.20.pdf |

## Security 

This data is freely available to the public.

## Contact

This repository was compiled and maintained by Valentine Garza at UW Seattle. Contact her at valgarza@uw.edu.
