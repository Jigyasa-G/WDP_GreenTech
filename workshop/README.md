# Predict solar energy usage with Machine Learning Designer.

## Overview

In this workshop you will learn how to create a predictive machine learning model through the [Azure Machine Learning designer](https://docs.microsoft.com/en-us/azure/machine-learning/concept-designer).
You will be able to forecast the production of solar energy in a panel, based on climatic data and with it start on your way to a more sustainable life.

| **Project Goal**              | *Learn about Machine Learning model and how to train and deploy a predictive model*                                    |
| ----------------------------- | --------------------------------------------------------------------- |
| **What will you learn**       | Identify use cases for predictive models linked to sustainability.The use of technology in promoting environmental sustainability.                                        |
| **What you'll need**          | Internet Connection, an [Azure account](https://azure.microsoft.com),ability to navigate the Azure portal,basic concepts of Python and Pandas|
| **Duration**                  | 1-1.5 hours                                                               |
| **Just want to try the app or see the solution?** | [Reference Notebook](https://ml.azure.com/fileexplorerAzNB?wsid=/subscriptions/90617110-25a5-404c-8888-29477a22fe42/resourceGroups/ExamPractice/providers/Microsoft.MachineLearningServices/workspaces/AI900-practice&tid=84c31ca0-ac3b-4eae-ad11-519d80233e6f&activeFilePath=Users/ANDREW.CHAN/german_renewable_data_prep.ipynb)                          |
| **Slides** | [Powerpoint](slides.pptx)                          

## Pre-Learning
- [Get started with AI on Azure](https://docs.microsoft.com/en-us/learn/modules/get-started-ai-fundamentals/).
- [Azure Machine Learning designer](https://docs.microsoft.com/en-us/azure/machine-learning/concept-designer).
- [Use automated machine learning in Azure Machine Learning](https://docs.microsoft.com/es-mx/learn/modules/use-automated-machine-learning/).
- [The Principles of Sustainable Software Engineering](https://docs.microsoft.com/en-us/learn/modules/sustainable-software-engineering-overview/).

Acknowledgements: 
- Credits to Hugo Ferreira's article on renewable energy prediction in Germany, which is the basis for this workshop: Blog: https://medium.com/hugo-ferreiras-blog/predicting-wind-and-solar-generation-from-weather-data-using-machine-learning-998d7db8415e; Code: https://nbviewer.org/github/hugorcf/Renewable-energy-weather/blob/master/renewable.ipynb


## What students will learn

1. Students will be skilled at: 
        Get an introduction to machine learning
        Use the automated machine learning capability of Azure Machine Learning to train and deploy a predictive model.
        
2. Students will be able to independently use their learning to:
        Identify use cases for predictive models linked to sustainability.

3. Students will undersand the concepts of : 
        The use of technology in promoting environmental sustainability. 
        


## Video walk-through. 

![image of completed project](images/placeholder.png)
>🎥 Click this image to watch EcoWatch team walk you through the workshop. 

## Pre-learning
- [Introduction to Python](https://docs.microsoft.com/en-us/learn/modules/python-data-science)

- [Pandas for Data Science](https://docs.microsoft.com/en-us/learn/modules/pandas-data-science)

- Manipulate and Clean Data on Python [workshop by Ornella](https://github.com/microsoft/workshop-library/blob/main/full/clean-prepare-data-python/README.md) 

## Prerequisites

- An [Azure account](https://azure.microsoft.com)

- An active [Azure subscription](https://azure.microsoft.com/en-us/free/)

- [Azure Portal](https://azure.microsoft.com/en-us/features/azure-portal/)

- Basic knowledge of [Python](https://www.python.org/downloads/).


## Milestone 1: Introduction to Machine Learning and Regression Models. 

### Machine Learning
Machine learning is the foundation of most AI solutions, using math and statistics to build predictive models for unknown values. 

Machines learn from data, every day we create a large amount of information that can be collected and used by data scientists to train a machine learning model and create predictions and inferences based on the relationships found in the information.

[![workshop walk-through](./images/images.png)](https://www.microsoft.com/en-us/videoplayer/embed/RE4xAok?postJsllMsg=true)
>🎥 Click this image to watch several examples of how a machine learning model works. 

### Regression models in machine learning

The Regression is a form of machine learning that is used to predict a numeric label based on an item's features,  in which you train a model using data that includes both the features and known values for the label, so that the model learns to fit the feature combinations to the label. Then, after training has been completed, you can use the trained model to predict labels for new items for which the label is unknown.


[![workshop walk-through](./images/Regresion_Logol.png )](https://docs.microsoft.com/en-us/learn/modules/understand-regression-machine-learning/)
>🔎 Click this image, to learn more about regression models in machine learning, 


## Milestone 2: Introduction to Sustainability in Machine Learning

Among the great challenges we have today is the fact of promoting sustainability within our lives to face problems such as climate change and carbon emissions. 

In an effort to generate change, we have made this workshop so that you can see how feasible it is to use solar panels in a region based on information from a region and thus have an energy generation without emissions that is more friendly to the environment.

You can also be an agent of change within your projects by taking into account the [eight principles of sustainable software engineering](https://docs.microsoft.com/en-us/learn/modules/sustainable-software-engineering-overview/).

![workshop walk-through](./images/visual-greentech.jpeg)
>♻️ [Visual Guide: To Sustainable Software Engineering](https://techcommunity.microsoft.com/t5/green-tech-blog/a-visual-guide-to-sustainable-software-engineering/ba-p/2130034) 


## Milestone 3: Getting the Dataset


Next, you will integrate machine learning with sustainability by predicting the renewable energy output with weather and renewables data from Germany -- you can imagine how this is relevant for an energy grid planner managing energy production in a country. 

Note: To directly download the cleaned datasets (joined from the weather and time series data), see [here](https://github.com/NikoMagafi/WDP_GreenTech/blob/main/workshop/solution/combined_german_renewable.csv)

Otherwise, to perform the data cleaning from scratch, download the two datasets that will be used in this dataset
(1) Time series wind and solar production in hourly resolution in 2016 (can be downloaded in our [GitHub folder](https://github.com/NikoMagafi/WDP_GreenTech/blob/main/workshop/solution/time_series_60min_singleindex_filtered.csv), or directly from the source, click the picture:   
[![time-series_data](https://user-images.githubusercontent.com/88496317/159603190-1fa6583e-11af-4003-ae43-67138a2e84dc.png)](https://data.open-power-system-data.org/time_series/2017-03-06)

(2) Weather data in Germany in 2016, can be downloaded in our OneDrive [link](https://hkustconnect-my.sharepoint.com/:f:/g/personal/agchan_connect_ust_hk/Ei9Zm1rJSgxEiKS1y7ZlD88BrAVL7gmXOvi_kML54ahp2w?e=h3Amxu), or directly from the source, following from the procedures in this picture (click the picture to be redirected) [![weather](https://user-images.githubusercontent.com/88496317/159603599-8bc5890e-53d3-40ec-b517-0e3e37812f40.png)](https://data.open-power-system-data.org/weather_data/2020-09-16) 



## Milestone 4: Data Preprocessing

Again, to directly download the cleaned and combined datasets (joined from the weather and time series data), see [here](https://github.com/NikoMagafi/WDP_GreenTech/blob/main/workshop/solution/combined_german_renewable.csv)

------If you've downloaded the weather and time series datasets separately ---------- 
We will explore the dataframes, create new columns with groupby, visualize relationships between variables, work with missing data and combine two datasets into one dataset to be fed to our machine learning model

### Time series data 
```
production = pd.read_csv("time_series_60min_singleindex_filtered.csv", usecols=(lambda s: s.startswith('utc') | s.startswith('DE')),parse_dates=[0], index_col=0)

```

### Weather data 
``` 

Importing the data: 
weather = pd.read_csv("weather_data_result_GER_2016.csv",
                     parse_dates=[0], index_col=0)
```

### Combined dataset

```
# merge production_wind_solar and weather_by_day DataFrames
combined = pd.merge(production_wind_solar, weather_by_day, how='left', left_index=True, right_index=True)

# drop redundant 'T (C)' column
combined = combined.drop('T (C)', axis=1)
```

## Milestone 5: Create and run training pipeline and Understand and Test the model.

### Model Building 
With the combined dataset, we can build our model predicting solar and wind energy output with the low-code machine learning platform AZ ML Designer. We will select specific columns for model training for the wind and solar energy prediction respectively. Data wil be normalized with min-max normalization, split to training and test sets, so as to prepare for model training on our linear regression model. 

![image](https://user-images.githubusercontent.com/88496317/159605985-57c3142b-bb1d-4137-9084-663b5b0cad0b.png)

### Evaluation of the model 
Model evaluation is as simple as dragging the scoring and evaluation nodes to the ML Designer. Wohoo, even without complex deep learning models, our linear regression model scored well with a 0.88 and 0.95 R squared on the wind and solar energy datasets respectively! Not bad for such a simple model!
![model_eval](https://user-images.githubusercontent.com/88496317/159606601-173b8e51-4ebf-4d67-84f8-7b8fa8c8225d.png)


## Milestone 6: Deploy a model as a service. 
We will submit our training pipeline for deployment, then test the model with sample inputted data from 2017. With Azure, we are able to process, train and deploy in the cloud easily and integrate our prediction results with external platforms. 

Wind model: 
![wind_pipeline](https://user-images.githubusercontent.com/88496317/159607398-65cbb2d3-fbbf-45ba-83a9-c16219d09775.png)

Solar model:
![solar_pipeline](https://user-images.githubusercontent.com/88496317/159607486-6c99d128-e305-478a-b227-3d54a973ea19.png)

With Azure, we can link our real time prediction with a centralized energy production system in an electricity grid dynamically adjust energy production, hence reduce energy and carbon wastage, advancing sustainability from its roots!

## Test your knowledge. 
You have come a long way in your learning journey, it's time to put your knowledge to test and prove that you have learnt it right. Attempt a quick quiz on *Kahoot*
[here](https://kahoot.it/challenge/04702208?challenge-id=c8b92fa6-4ccf-4cf3-abb7-425034be7dda_1647843077705).



## Optional Transfer knowledge activity

Now that you have learned a little more about the use of machine learning and how it can help us achieve a more sustainable life, use this workshop to teach your friends or colleagues to raise awareness about the use of renewable energy with this [slides](./Slides.pptx). 


## Feedback

Be sure to give [feedback about this workshop](https://forms.office.com/r/MdhJWMZthR)!

[Code of Conduct](CODE_OF_CONDUCT.md)

