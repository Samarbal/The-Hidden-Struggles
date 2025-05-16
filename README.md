
# The Hidden Struggles: How External Factors Impact University Students’ Academic Success in Gaza, A Data-Driven Approach



Presented by: Samar Balousha

Tutor: Ameer Alhelwani 

Mentor: Abduulrahman Shater

## Project Description

In Gaza, academic success often hinges on more than just classroom effort, as external challenges like electricity shortages, poor internet access, financial struggles, and mental health issues deeply impact students. This project uses a reality-inspired dataset and interactive Power BI dashboards to uncover patterns that hinder GPA and on-time graduation. By blending empathy with analytics, aim to provide clear, data-driven insights that empower universities to better understand students’ struggles and implement equitable support systems. The goal is to bridge raw data with smarter, compassionate interventions for those facing structural limitations.

## Dataset Description

The dataset is a simulated representation of 500 university students in Gaza, created using Python (NumPy, Pandas) in Google Colab, to reflect real-life student conditions across five key areas:

1. Demographic Information(age, gender, major,  family Income)
2. Academic Performance (GPA,  Graduated On Time , Study Hours/Week  )
3. Access to Resources (Electricity Hours/Day,  Internet Quality, Has Laptop,  Access to Textbooks, Study Space Availability)
4. Health and Wellbeing (mental and physical health issues ,  Food Security Level)
5. Challenges( Has Part-Time Job, Lost Their House  , Commute Time, Displacement Status)

## Data Preperation 
1. Adding a GPA Category:  A new categorical variable  created based on GPA scores

2. Adding Risk Factors: To measure external challenges affecting academic success, the following binary flags (0/1) were created

3. Total Risk Factors: A new variable was calculated by summing up all risk factor flags for each student , the result is out of 10.

## Data Visualization 

           
![vis1](https://github.com/user-attachments/assets/33377e19-6fa4-4508-b697-8d736546a5ce)


![vis2](https://github.com/user-attachments/assets/4ce6a251-ca6b-48f8-ad16-dad27e4fa5fd)


![vis3](https://github.com/user-attachments/assets/0278227d-3a14-461f-b736-86e9667a1803)


## Linear Regression Analysis 
               
A linear regression model was built to predict GPA based on three independent variables: Study Hours/Week, Electricity Hours/Day, and Internet Quality.

### Regression Statistics Analysis 


| Multiple R  |   0.667172612  | The correlation coefficient is approximately 0.67, shows a strong positive correlation between the  dependent variable (GPA) and independent variables (Study Hours/Week, Electricity Hours/Day, Internet Quality).                  |
|---------------------|-------------|----------------|
|R Square  | 0.445119295 | Values closer to 1 suggesting a better model fit. R2 is approximately 0.44, which means that around 44.5% of the variance in GPA can be explained by the model. |
| Adjusted R Square   | 0.441763161    | The adjusted R² is 0.4418, indicating that the model’s predictors reliably explain GPA without overfitting.  |
|Standard Error | 4.062353152  |4.06 indicates the average distance between the actual GPA values and the values predicted by the regression model,  it is a lower value suggests better model accuracy.      |
| Observations    | 500     |  The total number of data points (rows)        |


### ANOVA Analysis 

| Regression df   |  3  | Three independent variables were used (Study Hours, Electricity Hours, Internet Quality).     | 
|-------|---------|-------|
| Residual df | 496   |Remaining degrees of freedom from the 500 observations. | 
|  F-statistic  |  132.63 | A very high F-value, showing the model significantly explains the variance in GPA.   |
|  Significance F       |   4.3368E-63   |   Extremely small p-value (< 0.05), indicating the model is highly statistically significant. Reject the Null Hypothesis .   |  

### Regression Equation

The projected GPA is calculated as:
Projected_GPA = 
    64.55326 
    + 0.637298 * 'Gaza_Students_Data'[Study Hours/Week] 
    + 0.308716 * 'Gaza_Students_Data'[Electricity Hours/Day] 
    + 0.76292 * 'Gaza_Students_Data'[Internet Quality]

This shows that each additional study hour increases GPA by 0.64 points, each electricity hour by 0.31 points, and good internet quality by 0.76 points.

![vis4](https://github.com/user-attachments/assets/a5a63c76-e869-4054-b3d9-a55557ce00cf)

##  Future Enhancements
 * Collect real student survey data from multiple universities across Gaza
  * Track semester-by-semester performance for trend analysis
  * Ask for Feedback: Talk to students and teachers to improve the project.
* Convert to AI model 


## References
* Data Source : Simulated dataset generated with Python (NumPy, Pandas) using Google Colab Notebook 
* Data Preparation and Analysis :Microsoft  Excel
  https://unrwaedu-my.sharepoint.com/:x:/g/personal/m_baelousha_unrwa-edu_org/EZPa-9zV6OVEiEx5z3IhPxwB_BsGABw8FVIfVtdRH2LaTA?e=hbYfQ0

* Data Visualization : Microsoft  Powerbi 
https://unrwaedu-my.sharepoint.com/:u:/g/personal/m_baelousha_unrwa-edu_org/EcgSbti96ppKtzyi_ZBuvgcBtULpjNy7z09gVCg7LSlwLQ?e=UGo4j8 
* Further Reading:
https://www.ablebits.com/office-addins-blog/linear-regression-analysis-excel/
https://www.geeksforgeeks.org/power-bi-tutorial/ 

## Video 
[Video link](https://drive.google.com/file/d/18CfyFe53hiUltdKN-rVrNFXV2XtuyhPq/view?usp=drive_link)
