# H1N1 and Seasonal Flu Vaccines


## Business Understanding

The COVID-19 pandemic reshaped our understanding of how society responds to a common crisis and recentered the conversation around public health. In order to provide guidance for future public health efforts, this analysis revisits the 2009 public health response to the H1N1 influenza virus and attempts to understand how people’s backgrounds, opinions, and health behaviors are related to their personal vaccination pattern.


## Data Understanding

**H1N1**

Beginning in spring 2009, a pandemic caused by the H1N1 influenza virus, colloquially named "swine flu," swept across the world. Researchers estimate that in the first year, it was responsible for between 151K - 575K deaths globally. A vaccine for the H1N1 flu virus became publicly available in October 2009. 

In late 2009 and early 2010, the United States conducted the National 2009 H1N1 Flu Survey. This phone survey asked respondents whether they had received the H1N1 and seasonal flu vaccines, in conjunction with questions about themselves. These additional questions covered their social, economic, and demographic background, opinions on risks of illness and vaccine effectiveness, and behaviors towards mitigating transmission. 

**Survey Data**

Using this survey data, acquired from the [National Center for Health Statistics](https://www.cdc.gov/nchs/nis/data_files_h1n1.htm), the predictive model below attempts to classify whether or not an individual received an H1N1 vaccination based on various personal opinions and behaviors.

### Target
Of approximately 27K respondents, only 21% had opted to receive the H1N1 vaccine (compared to 47% for the seasonal flu vaccine). 

### Features

The survey covered 35 unique features that we grouped into four categories:
    - vaccine opinion, such as general knowledge of H1N1 and concern of getting sick from the virus or vaccine
    - medical concern, such as if doctors' recommendedation on receiving the vaccine or having a chronic medical condition
    - behavioral patterns, such as avoiding large gatherings or wearing face masks
    - demographics, such as age, employment, location, etc.

Vaccination levels remained fairly consistent across different classes of behavioral patterns and demographics, while vaccine opinions and medical concern seem to have a wider variance in vaccination levels across different features classes.
A notable outlier in the demographic features is employment occupation & industry where certain classes appeared to have much higher vaccination levels than the average.

## Modeling & Evaluation

The final model, a random forest classifier, maximizes the precision score, a measure of the true positive rate. This model focuses on minimizing the false positives- that is to say the prediction someone did get the vaccine when they actually did not.

After running  basic predictive models and then tuning parameters to maximize the precision score, the model reached 83% accuracy with 70% precision.

## Conclusion

Using this information, we can focus in on the most significant features, respondent's opinion of the vaccine and illness risk as well as medical concern levels. These features can help guide formaton of surveys for private ventures that may not be able to gather personal demographic information as government agencies are able to. This can also guide media advertising to target populations that may be disinclined to get vaccinated. It would also be beneficial to do more research on which combination of features most minimizes the false positives and finds the most vulnerable populations.
