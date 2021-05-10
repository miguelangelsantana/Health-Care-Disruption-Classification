
# Disruptions in Healthcare due to COVID-19
#### Observing disruptive trends | Kaggle & Data.gov

Author: Miguel Santana

### Project Methodology
COVID-19 caused major disruptions all over the world. In order to work toward normalcy, we must identify and understand pain points before building tools and resources that help vulnerable populations manage the new challenges of the world. This analysis will explore two datasets in order to gain a deeper understanding of how COVID-19 effected the availability of health care as well as the availability of mental health in the United States. 

### Data and Analytical Structure
The first dataset is a collection of survey data addressing Mental Health Care (last 4 weeks) in the United States. The dataset is provided by the Centers for Disease Control and Prevention via Data.gov and can be found [here.](https://catalog.data.gov/ar/dataset/mental-health-care-in-the-last-4-weeks) The dataset was collected as part of the Household Pulse Survey. Additional information outlining the specifics of the survey can be found [here.](https://www.cdc.gov/nchs/covid19/pulse/mental-health-care.htm)

The second collection is a data summary funded by the Bill and Melinda Gates Foundation. The dataset is titled Premise General Population COVID-19 Health Services Disruption Survey 2020 and can be found via Kaggle [here.](https://www.kaggle.com/vishalsiram50/covid19-health-services-disruption-survey-2020) The project analysis will follow the OSEMN framework: Obtain, Scrub, Explore, Model and Interpret.

![!](/images/OSEMN.png)

### Data Processing and Modeling

Once data processing (filling nulls, feature engineering, etc) was completed, each of the datasets was reduced to highlight demographics that specifically 'needed' healthcare and illustrated whether they did or did not receive it. Categorical variables were encoded and statistical analysis was completed using Pycaret.

## Exploratory Data Analysis | Tableau Public

<div class='tableauPlaceholder' id='viz1620617419679' style='position: relative'><noscript><a href='#'><img alt=' ' src='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;Ka&#47;KaggleCOVID-19Dataset&#47;OVERVIEW&#47;1_rss.png' style='border: none' /></a></noscript><object class='tableauViz'  style='display:none;'><param name='host_url' value='https%3A%2F%2Fpublic.tableau.com%2F' /> <param name='embed_code_version' value='3' /> <param name='site_root' value='' /><param name='name' value='KaggleCOVID-19Dataset&#47;OVERVIEW' /><param name='tabs' value='yes' /><param name='toolbar' value='yes' /><param name='static_image' value='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;Ka&#47;KaggleCOVID-19Dataset&#47;OVERVIEW&#47;1.png' /> <param name='animate_transition' value='yes' /><param name='display_static_image' value='yes' /><param name='display_spinner' value='yes' /><param name='display_overlay' value='yes' /><param name='display_count' value='yes' /><param name='language' value='en' /></object></div>

The full dashboard can be viewed via Tableau Public [here.](https://public.tableau.com/views/KaggleCOVID-19Dataset/OVERVIEW?:language=en&:display_count=y&:origin=viz_share_link)                
# Statistical Model | Pycaret
## Gradient Boosting Classifier

![png](/images/results.png)

### Class Report

![png](/images/ClassificationReport.png)

### AUC

![png](/images/AUC.png)

### Confusion Matrix

![png](/images/ConfusionMatrix.png)

### Feature Importance

![png](/images/FeatureImportance.png)

## Interpret Model | SHAP

![png](/images/SHAP.png)

### Highlighted Feature | Education Level

![png](/images/EducationLevel.png)

### Highlighted Feature | Gender

![png](/images/Gender.png)

## Conclusion
Our analysis is centered around dataset classifiers that negatively affect our target variable (per SHAP value analysis). Lower target variables represent limited (or no health care) received by individuals who explicitly needed health care pre/post COVID-19. 

Individuals affected by limited (or no health care) have one or more of the following qualities:
* Reason for Missing Dr. Appointment | Fear of contracting COVID-19
* Do not currently take medication
* Live in countries with lock down restrictions
* Not part of the labor force pre or post COVID-19
* Students
* Women
* Self Employed

### Limitations

Online survey responses naturally carry a bias due to the fact that certain groups of individuals are not as tech savvy as others. As a result, the representation of these groups is limited. From a cultural perspective, some individuals (depending on the country) are less willing to be honest on surveys. This may be due to regulatory influence or a general mindset passed down through generations (don't complain about things you can't change). 

### Future Work
Future work should include resource development for individuals in the 20-30 age category with a special focus on college students. This specific demographic seems especially affected with respect to limited (or no) health care. 

### Further Information
Please review the narrative of our analysis in [our jupyter notebook](./healthcare_notebook.ipynb) or review our [presentation](./presentation.pdf)

For any additional questions, please reach out via email at santana2.miguel@gmail.com, on [LinkedIn](https://www.linkedin.com/in/miguel-angel-santana-ii-mba-51467276/) or on [Twitter.](https://twitter.com/msantana_ds)

##### Repository Structure:

```

├── README.md               <- The top-level README for reviewers of this project.
├── healthcare_notebook.ipynb     <- narrative documentation of analysis in jupyter notebook
├── presentation.pdf        <- pdf version of project presentation

```
