---
name: Visualizing Online Education Effectiveness
tools: [Python, HTML, Altair, vega-lite]
image: assets/pngs/students.png
description: An interactive dashboard that correlates online education performance to multiple socio-demographic variables
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---

# Gathering insights on online education effectiveness through visualization tools
##### _Article by Lucas Borges dos Santos and Oluwatoyosi Awe_.   Dec 5, 2022
<br>

The COVID 19 pandemic has reshaped the educational system in nearly any country of the world. Restrictions of in-person activities have forced the creation of entirely new pedagogic approaches, and many of these remain partially active even after 2.5 years of pandemic. Nonetheless, the development of new remote-learning approaches it is a challenging task, since it depends on technologic resources, such as computers, laptops, good internet connection, and proper training for teachers and students.

Poor communities were the first to show a significant decrease in education quality, due to the lack of such resources. In addition, each demographic segment of the society have adapted differently to these new systems of remote-learning, given the conditions they have been exposed to. However, quantifying the real impact on learning remains a challenge.

In this project, we will be searching for interesting patterns on the most vulnerable demographic groups in the context of online educational effectiveness within a under-developed country. For this purpose, we are going to explore a publicly-available dataset and build an interactive dashboard for visualizing multiple independent variables from this data.

The dataset we are going to use is called "Students Adaptability Level in Online Education", which evaluates online learning performance of Bangladesh students during the COVID-19 pandemic. This data was obtained from [Kaggle](https://www.kaggle.com/datasets/mdmahmudulhasansuzan/students-adaptability-level-in-online-education), and belongs the the paper "Students' Adaptability Level Prediction in Online Education using Machine Learning Approaches" ([Suzan et al., 2021](https://www.researchgate.net/publication/355891881_Students'_Adaptability_Level_Prediction_in_Online_Education_using_Machine_Learning_Approaches)).

<br>
<vegachart schema-url="{{ site.baseurl }}/assets/json/students_dash.json" style="width: 100%"></vegachart>
[Click here]() to see the source code underlying this dashboard
<br>

### What can we get out of these charts?


The dashboard enabled the identification of some interesting correlations within our students dataset: 

* The adaptability distribution varied among different school levels: College students have been identified as the lowest adapted with online-learning, followed by university students and school, respectively. 

* Poor, mid and rich students are not equaly represented in our dataset: There is a considerably larger number of students in the "mid" category. This might be an artifact of how the data was collected (self-reporting), where students tend to not classify themselves in any of both extremes.

* At universities, the number of female students is considerably smaller than male. 

To support some of our findings, we searched for external sources of information around internet access and gender inequality in Bangladesh. The images below were extracted from the [Our World in Data](https://ourworldindata.org/) website and reveal some insteresting facts of this country:


* Indeed, women are minority within universities: Data from 2014 indicates that only 35% of STEM students were women. 

<img src="https://github.com/bslucas98/bslucas98.github.io/blob/main/assets/pngs/share-graduates-stem-female.png?raw=true" width="600"> 
Source: [Our World in Data](https://ourworldindata.org/grapher/share-graduates-stem-female?tab=chart&country=BGD)

* In addition, high poverty indices are reflected in the internet access in Bangladesh. Less than 30% of the population have used the internet in the last 3 months. 

<img src="https://github.com/bslucas98/bslucas98.github.io/blob/main/assets/pngs/share-of-individuals-using-the-internet.png?raw=true" width="600"> 
Source: [Our World in Data](https://ourworldindata.org/grapher/share-of-individuals-using-the-internet?tab=chart&country=BGD)

This observation supports our the fact that mid-class students are minority in our dataset. The study were data was collected surveyed <ins>students who have experienced online education during the pandemic</ins>, however low-income students most likely have been completely absent from school due to difficulties to access digital resources. Thus, they have also been underrepresented in this study from Suzan et al.

