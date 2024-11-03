# LITA_class
This is where i document my powerbi class project while learning Data Analysis with Incubator Hub
## Project title: Data Visualization using PowerBi

[project overview](#project-overview)

[data sources](#data-sources)

[Tools Used](#tools-used)

[Data Cleaning and preparations](#data-cleaning-and-preparation)

### Project overview
---
The project is about checking for the attrition rate and attrition patterns in a particular organization using a data provided by the HR.

### Data Sources
The HR data used was provided by the tutor to use in class. The data is HR data.xlsx.

### Tools Used
PowerBi- It was used for the following:
- Data cleaning using the transform data ribbon.
- DAX functions using measures, conditional columns and calculated columns

 ### Data Cleaning and Preparations
The data was cleanes using Transform data. The first column was promoted as headers. The data type was changed to the appropriate one.

 ### Data Analysis
 This is where I include basic lines of DAX functions used during analysis;

 ```Powerbi
= Table.AddColumn(#"Changed Type1", "Attrition number", each if [Attrition] = "Yes" then 1 else 0)
= Table.AddColumn(#"Changed Type2", "Age sort", each if [CF_age band] = "Under 25" then 1 else if [CF_age band] = "25-34" then 2 else if [CF_age band] = "35-44" then 3 else if [CF_age band] = "45-54" then 4 else 5)
= Table.AddColumn(#"Changed Type3", "Satisfaction rate", each if [Job Satisfaction] = 1 then "Very Dissatisfied" else if [Job Satisfaction] = 2 then "Dissatisfied" else if [Job Satisfaction] = 3 then "Satisfied" else "Very Satisfied")
```

### Data Visualization
![Screenshot (26)](https://github.com/user-attachments/assets/aa6fc5d6-dcd4-49d1-b1e0-1a7f9bd56618)

![Screenshot (25)](https://github.com/user-attachments/assets/e6381132-6652-4d19-97fc-34e5afe85124)

### Observation from Analysis


