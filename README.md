# LITA_class
This is where i document my powerbi class project while learning Data Analysis with Incubator Hub
## Project title: Data Visualization using PowerBi

[project overview](#project-overview)

[data sources](#data-sources)

[Tools Used](#tools-used)

[Data Cleaning and Preparations](#data-cleaning-and-preparations)

[Data Analysis](#data-analysis)

[Data Visualization](#data-visualization)

[Observation from Analysis](#observation-from-analysis)

[Recommendation from Analysis](#recommendation-from-analysis)

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
The attrition rate in the organization is 16%. The education field with the highest attrition count is life sciences with 89 employees, the education field with the least attrition is Human resources with a count of 7 employees. The department with the highest attrition count is the R&D department with a total of 133 employees and the department with the least attrition count is the HR department with attrition count of 12. It is noticed that more males (150) left the organization than females(87). This could be because men are more likely to look for 'greener patures' than women would.

The age group with the highest attrition is 25-34 with a total of 112 employees that have left within that age group. The age group with the lowest attrition ia persons above 55 with a count of 11 employees that have left. This could be because at age 25 to 34, people's careers are transitioning and they easily switch location, jobs and careers. Atage 55, people are already settled.They have stable locations because they have built structure around their jobs and locations, so they are least likely to move.

The majority(73) of people that left are those that said they were satisfied with their jobs followed by those that said they were dissatisfied with their jobs. The job roles with the highest attition is the laboratory technician with 62 employees that left and the job roles with the lowest attrition is research director with a count of 2.

### Recommendation from Analysis
