# DeepLearners-California-Unemployment


## Group 1 - Team Members:
	Hossein Arjomandi
	Nic Prate
	Tixian Wang
	Zijian Zhen


## Important Links

### Presentation Slides: [LINK](https://docs.google.com/presentation/d/10_IF2QwRAoPUNcJvS8QGHZVucznnAlRixQ_QTgBElMU/edit?usp=share_link)

### Presentation Video: [LINK](https://drive.google.com/file/d/1lgLFlBXyPYRjU28Sa_Kct4FGcZpt1Qta/view?usp=share_link)

### Codes:
* Pickle Data:
[Pickle Data](https://colab.research.google.com/drive/1-m5Q3feuwhKE0EGyhfFGhhCrQrhkpR6e?usp=share_link)

* Descriptive statistics and data visualization:
[Descriptive Analysis](https://colab.research.google.com/drive/1rkF6LH0oFIWXjYuC1qho-wEhJzbHqbFQ?usp=share_link)

* RNN data cleaning:
[RNN Dataframe](https://colab.research.google.com/drive/1EAYw0sHlh9OC6zQwd7FyG9Ya3AdR4D2q?usp=share_link)

* Linear Regression approach 1 training:
[Linear Regression approach 1](https://colab.research.google.com/drive/1oM8zzHqWP6Saj-cb35MLBunZvHgfOc2p?usp=share_link)

* Linear Regression approach 2 training:
[unadjusted data version](https://colab.research.google.com/drive/1iousQTB540GEg_d6ulWvTzk0a_bNvcm-?usp=share_link), [adjusted data version](https://colab.research.google.com/drive/14md-aSzQm1PyPUT00kRjQychWS5VyOMx?usp=share_link)


* RNN approach 1 training:
[RNN approach 1](https://colab.research.google.com/drive/10HjzPPWp1fYPeyBTCheRSUBuJUA33Uoa?usp=share_link)

* RNN aproach 2 training:
[RNN approach 2](https://drive.google.com/file/d/1b4s1dLu3lohGdXYhPEGEN9MsZ1QLFpmv/view?usp=share_link)

* Drawing prediction:
[RNN Dataframe](https://drive.google.com/file/d/1tsy_miQmA-s8YupGd_iZW_GOHMw05FIz/view?usp=share_link)

##  Environment and Dependencies
You don't need any dependencies, just open the notebooks on Colab!


## Problem explanations:
We are going to use California's unemployment data for the past few decades to predict the ones for the next few years.


## Dataset: [California’s Unemployment Rate](https://data.ca.gov/dataset/local-area-unemployment-statistics-laus/resource/b4bc4656-7866-420f-8d87-4eda4c9996ed)

|Feature|Description|
|:---|:---|
|||
|Month| month of data source, range from January to December
|Year| year of data source, range from 1976 to 2022
|Date| date of the data source, range from 1976/01/01 to 2022/09/01
|Area Name|categorical feature, totally 1050 different area names.
|Area Type|categorical feature, totally 6 different area types.
|Total Labor Force| number of labor force in the given area
|Employment| number of employment force in the given area
|Unemployment| number of unemployment force in the given area
|Unemployment Rate| Unemployment / Total Labor Force
|Seasonally Adjusted|whether the data is modified to eliminate the effect of seasonal and calendar influences, the gap between the average unemployment data of each months can be seen in [this graph](https://drive.google.com/file/d/1sPFB2c6Md0DVdGTEzMn0fZr9mZeM7lAF/view?usp=share_link).


### Descriptive statistics:
We include the mean, standard deviation, minimum, maximum, and the correlation between `Total Labor Force` and `Unemployment Rate` for each of the 1050 areas and the 4 are types with non-adjusted data. 

You can check the detailed descriptive statistics in the following two links:
* [Descriptive statistics group by area name](https://drive.google.com/file/d/1TSYgF4YNSjIez-SfV-YFrfZGcie7aj0m/view?usp=share_link)
* [Descriptive statistics group by area type](https://drive.google.com/file/d/1BfYVFCJYRfRWSnJryO8pJ8ezdBt_g-vR/view?usp=share_link)

### Data visualization
Here is the visualization of the historical unemployment rate of 60 selected areas in the dataset.
* [Data visualization](https://drive.google.com/file/d/1np8XMDb93efXpkBFgxBLIoGKs1LsEvL0/view?usp=share_link)
* [Gap between the average unemployment data of each months](https://drive.google.com/file/d/1sPFB2c6Md0DVdGTEzMn0fZr9mZeM7lAF/view?usp=share_link)



## Experiments & Results

### Linear Regression - approach 1

We trained Linear Regression based on each unique area as a baseline model in our experiment. 


Code for Linear Regression approach 1: [link](https://colab.research.google.com/drive/1oM8zzHqWP6Saj-cb35MLBunZvHgfOc2p?usp=share_link)

Here is the MSE loss for Linear Regression models trained on each of the area names, we only show 50 of them.  
* [MES Loss for Linear Regression](https://drive.google.com/file/d/1yzJnnqBTewDf3Xf3PzJKeJAczflkmlcQ/view?usp=share_link)

The preformance of the model is not ideal, and it's not able to capture small-local or large-global peaks and valleys.



### Linear Regression - approach 2

We also trained a Linear Regression on all data (adjusted and unadjusted).

Code for Linear Regression approach 2 on non-adjusted data: [link](https://colab.research.google.com/drive/1iousQTB540GEg_d6ulWvTzk0a_bNvcm-?usp=share_link)

Code for Linear Regression approach 2 on adjusted data: [link](https://colab.research.google.com/drive/14md-aSzQm1PyPUT00kRjQychWS5VyOMx?usp=share_link)

The graph of MSE loss for Linear Regression approach 2 trained on non-adjusted data: [link](https://drive.google.com/file/d/1FjaXWjcZg8Tv_dHIWrqgWN8raihKQ9Al/view?usp=share_link)

The graph of MSE loss for Linear Regression approach 2 trained on adjusted data: [link](https://drive.google.com/file/d/1FlqEjAyo-niN08kJ_9ynYKCTgR__QMDi/view?usp=share_link)

The prediction of California unemployment rate: [unadjusted](https://drive.google.com/file/d/1FeD3-Pll3R3IuGLXeHYGtD9YNrRLg9sN/view?usp=share_link), [adjusted](https://drive.google.com/file/d/1FoJedCKqGxaX1SWzKJEl8OJQrxtZJB2c/view?usp=share_link)

The prediction of Los Angeles unemployment rate: [unadjusted](https://drive.google.com/file/d/1FfCGlKq089Hz89SzE4PgZYBd2l8Rwcls/view?usp=share_link), [adjusted](https://drive.google.com/file/d/1FpoCO9axrJYjUYWAZLpfh8BZmUIZuJWZ/view?usp=share_link)



### Recurrent Neural Network - approach 1


The effects of mini-batch learning and different optimizers is included in the Colab Notbook, please click into the [Colab notebook link](https://colab.research.google.com/drive/10HjzPPWp1fYPeyBTCheRSUBuJUA33Uoa?usp=share_link). 

Also, we provided the detailed performance for the model on each area, please click in to [this link](https://drive.google.com/drive/folders/1AJ3zcFMPCqdPizBU_LNWqWSiHXTHBQIU). Sub-folders in this link contains the training and validation loss figure of models build on each area. 

The prediction of California unemployment rate: [link](https://drive.google.com/file/d/1fxG7JaZUOOLzqfQBiEzg2k0uxjI3NEGP/view?usp=share_link)


### Recurrent Neural Network - approach 2

Instead of training LSTM model for each area. We also trained a big LSTM model using multiple areas together.

We selected all regions with complete data from 1990 to 2022 to train the model. And also, to ensure the compatibility, we uses the same hyper-params as approach 1. And here is the losses for the LSTM model trained on the integrated data. We can see that, overfitting is mitigated. The validation and test loss is slightly smaller than that in approach 1. 

The code for RNN approach 2 training: [link](https://drive.google.com/file/d/1b4s1dLu3lohGdXYhPEGEN9MsZ1QLFpmv/view?usp=share_link)

The prediction of California unemployment rate: [link](https://drive.google.com/file/d/1yVR_c2B0uI_b1DN-a4bGWSM8hGDqUF8U/view?usp=share_link)




## Project Timeline and Milestones
### Milestone  10/23/2022:
1.  ~~Zijian: Create a repository with Readme.md as wanted~~
2.  ~~Hossein: Convert rows of dataframe to objects of appropriate attributes (one hot encoded, timestamp, integer). Then we have an array of objects~~
3.  ~~Nic: See if we can convert this array of objects to a single dataframe~~
4.  ~~Tixian: See how to pickle an object, be it an array of objects or a dataframe (depending on the answer to 3rd question we may need to pickle a dataframe or an array of objects)~~

### Milestone  11/06/2022:
1. ~~Drop date feature for linear regression.~~
2. ~~Try unemployment rate time series for each area as input for RNN~~
3. ~~Try unemployment rate and labor force in time series for each area as input for RNN~~
4. ~~Consider category data embedding for RNN~~
5. ~~RNN would be a good choice for times series data.~~
6. ~~Each timestamp only has partial observations, how does that work in RNN? What should the data that we feed into the RNN looks like?~~
7. ~~Is that possible if we just take California data as input?~~

### Milestone  11/20/2022:
1. ~~Data visualization and descriptive statistic~~
2. ~~Pickle data for time RNN model.~~
3. ~~Trained Linear Regression model on each of the area.~~
4. ~~Try RNN model.~~

### Milestone 11/29/2022:
1. ~~Build a deep learning model for the dataset~~
2. ~~Investigate effects of mini-batch learning~~
3. ~~Investigate effects of different optimizers~~
4. ~~Tune hyperparameters (training testing and validation)~~

### Milestone 12/9/2022:
1. ~~Train a LSTM on all data~~
2. ~~Train a LR on all data~~
3. ~~Prepare for the presentation~~

