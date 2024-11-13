# Project - 1 Thirsting for Treatment: Understanding Substance Abuse Treatment Deserts Through Data

## Project Overview
This study examines substance abuse treatment center admissions in 2019, exploring the geographical disparities and trendlines to identify regional patterns, underlying factors, and implications for policy-making and resource allocation.

## Healthcare deserts five dimension of access 
- Availability
- Accessibility
- Accommodation
- Affordability 
- Acceptability


## Data Source
 This study utilizes data accessible from [Substance Abuse and Mental Health Services (SAMHSA.gov)](https://www.samhsa.gov) to examine substance abuse treatment center admissions and their geographical distribution in 2019. The data available publicly was from 2020 and earlier.  We chose to look at the 2019 since it was not influenced by Covid restrictions.   

 1.  Information on demographic, clinical and substance use characteristics of persons admitted to treatment: [TEDS DATA Files](https://www.samhsa.gov/data/data-we-collect/teds/datafiles)

 1. facility data on substance use treatment services: [N-SSATS DATA Files](https://www.samhsa.gov/data/data-we-collect/n-ssats/datafiles?puf_id=47343)

 Note: Data files was not pulled into GitHub due to the size of the file.

 All the data is coded and required mapping to Key values for visualization purposes. 

## Visualizations
1.	Pie Charts: Illustrate the breakdown of treatment center ownership types, services types used in a particular state.
1.	Bar Graphs: Show treatment availability by region and wait times by state type.
1.	Maps: Highlight treatment deserts and provide an interactive view of treatment access across the U.S.

 ## Observations

1. We found that six US states have a lower than average access to treatment.
    1.  To understand the capacity available in each state. We created a capacity ratio by taking the total cases and total beds available we created a capacity ratio.  All states that fell one standard deviation above the mean threshold of 480 were  categorized as potential deserts. Those states are Arizona, Colorado, Delaware, Maryland, New Jersey and Vermont. 

    1. Map of the total bed capacity ratio by state. Red indicated the state was one standard deviation above the mean. 
![Tux, the Linux mascot](Image/Ratio_of_Total_Capacity_by_state.png
)
    1. Overall, the regression model suggests a moderate positive relationship between treatment center capacity and total cases, but also indicates that the model does not fully capture all the factors affecting total cases. You may want to explore additional variables or improve the model to increase the explanatory power (R-squared value) further.   
![Tux, the Linux mascot](Image/output_scatter_ration_bed_bystate.png
)

1. We reviewed treatment by age group to understand if there was availability of services by age group. People under 20 and over 65 years old have less treatment admissions by age group.   It suggests that further investigation is necessary to determine whether the observed lower treatment numbers are due to a lack of facilities in that group or if it is a result of fewer drug users in that population. A comprehensive study could help clarify the underlying factors contributing to these disparities in treatment access.
![Tux, the Linux mascot](Image/outputbyage.png
)

1. We also studied the wait time by state to understand if any had wait times greater than 30 days.  We found that several states on our target list of potential deserts wait times over 30 days.  We noted that Arizona didn't report wait times.   
![Tux, the Linux mascot](Image/output_waitGr30days.png
)


1. To understand accessibility deeper we reviewed the distribution of services provided by state.
Outpatient treatment made up the highest percentage of overall treatment by all states followed by rehabilitation services. 
    1. All States
![Tux, the Linux mascot](Image/output_case_disto_by_state.png
)

    1.  Arizona: We looked at the distribution of services for the target desert states and Arizona stood out since 97% of all treatment was outpatient treatment.This led us to conclude the reason they don't report wait times is the frequency of outpatient treatment and little to no wait for that treatment. 
![Tux, the Linux mascot](Image/output_case_distro_by_AZ.png
)

1. Affordability plays a key role in identifying a healthcare desert to understand affordability we reviewed the payment method of services received and ownership distribution.
    1. Payment method
        1. The teds data frame was filtered to remove cases that did not provide the payment method of treatment. 
        1. An ANOVA test was run to identify if there was any significant difference with a results F-statistic: 0.4675476751194555, P-value: 0.519637175760407
            1.  Due to the low F-statistic there is no significant difference in the types of services received. 
![Tux, the Linux mascot](Image/output_sevices_by_ins_type.png)

1. When reviewing the ownership distribution across all states and the Privately Owner categories of for profit and non-profit stood out.   A deeper studied of the cost between these categories would be needed to fully understand the impact.  However, the lack of federally funded faculties was noted. 
![Tux, the Linux mascot](Image/output_ownership_bytype_allstates.png
)

## Conclusion
There are six states in the US that stand out as potential deserts with Arizona and Colorado standing out due to the low availability of services other than outpatient in Arizona and long wait times in Colorado.   We recommend a deeper study in these states to identify the demographics of those getting treatment along with the cost across ownership of the facilities.  We would also recommend an effort to gain additional federal funding to increase the overall capacity of available beds in all 6 states identified as potential deserts. 

## Citation
Substance Abuse and Mental Health ServicesAdministration, Treatment Episode Data Set(TEDS): 2019. Rockville, MD: Substance Abuse and Mental Health Services Administration, 2021.

Substance Abuse and Mental Health Services Administration, National Survey of Substance Abuse Treatment Services (N-SSATS): 2019. Data on Substance Abuse Treatment Facilities. Rockville,MD: Substance Abuse and Mental Health Services Administration, 2020.

Brinzac, Monica, et al. “Defining Medical Deserts—an International Consensus-Building Exercise.” European Journal of Public Health, vol. 33, no. 5, 8 July 2023, academic.oup.com/eurpub/article/33/5/785/7221624, https://doi.org/10.1093/eurpub/ckad107.


