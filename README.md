![Header Image](https://github.com/mross715/MicrosoftProject/blob/main/images/readme%20image.png)
Source: freepik

# Predicting House Price in King County, Washington

## August 2021

Eric Denbin, Allison Gao

## General Overview and Business Understanding
This analysis uses historical data on houses sold in 2014 and 2015 in King County, Washington to predict housing price in the same county with respect to a myraid of factors such as square footage of the house and location. The purpose of the analysis is to provide actionable recommendations for home flippers seeking to purchase houses and flip them for profit. Our analysis shows that square footage of the house is an important factor such that increasing the house size will increase house price. Additionally, we found that house size's relationship to price needs to be analyzed in the context of the building quality as measured by the grading system used by the county. Home flippers can use this project’s findings to inform its business decision with respect to purchasing houses in King County. 

## Data 

###### Data Source
This project utilized a dataset from King County detailing houses sold in 2014 and 2015 with features that included price, location, square footage of the house,number of floors,and many other relevant housing related factors. 

###### Data Shape
The entire raw dataset contains 21,597 rows and 21 columns. Each row represents an house sale while each column specifies a feature such a number of floors in that house or year built. 

###### Data Preparation
We cleaned the dataset by dropping missing values, unoperational values such as questions, and outliers. We also created additional columns that are needed for analysis. This included interaction terms where we deemed that certain variables are better intepreted with another factor. For example, we created interaction term for building quality(as measured by grade) with square footage. Additionally, we logged certain variables in order to normalize them because they are not normally distributed. At the end of the cleaning process, the data contains 150,127 observations for analysis. 


## Data Analysis 

This project used multiple regression analysis to generate models that predict home sale price. We split the data into training and testing set so that we can train our data and test it on completely unseen data in order to understand how well our model does in predicting our response variable. summary statistics of various variables in the dataset. Anchoring our analysis on potential movie genres that Microsoft should consider, we examined how Microsoft can maximize ROI with respect to other factors. In particular, we focused on the following variables: release date, production budget, and worldwide gross. 


## Results 

Our cleaned and filtered dataset has a mean home price of $540,506. Furthermore, our best model contains 26 variables using approximately 11,000 observations. It explains about 78% of the variation we see in home price, our response variable. Additionally, our model saw an average error of $180,950 on our training data and an average error of $183,082 on our unseen data. 

The following three operable factors are statistically significant. We defined operable to mean features home flippers can operate on or fix. 

1. Square footage of the entire house
2. Building quality as measured by building grade ( 1 to 13)
3. Number of bathrooms

The following three non-operable factors are statistically significant. We defined non-operable to mean features home flippers cannot operate on or fix. However, home flippers can still exert decision over these factors. 

1. If a house is facing the waterfront 
2. Age of the house
3. House living space for the nearest 15 neighbors


###### Change in feature and its relationship to change in home price 

![Header Image](link)
We highlighted what happens when we increase a feature by one unit or one percentage point. For example, we see the among the three factors, one additional increase in bathroom generated the greatest change in price compared to the other two factors. 


###### Change in house square footage and its relationship to change in home price 

![Header Image](link)
Sale price increases by ~0.64% for every  1% increase in the house's square feet


###### Change in house square footage and its relationship to change in home price for different quality houses

![Header Image](link)
For a house with an average grade and at an average price ($540,506) if you increase the square footage of the entire living space by 1%, it will increase the sale price by  ~$5,400. 


###### Change in number of bathroom and its relationship to change in home price

![Header Image](link)
For a house and an average price, one additional bathroom will increase sale price by  ~$31,000. 



## Conclusion and Recommendations 

Results from this project’s analysis suggest the following three recommendations for home flippers to consider:

1. Start with location. We found that home price does differ whether or not a house is facing a waterfront. Additionally, such difference is also statistically significant between houses on the northern and southern part of the county. Even at the neighborhood level, the square footage of interior housing living space for the nearest 15 neighbors has an impact on house price. These three factors are helpful to consider as home flippers start the decision process. 

2. After a location is selected, we recommend that home flippers consider these three features that are operable as an effort to increase home price. 
    A. We found that increasing the house size is associated with an increase in house price. For example, a house that is at $540,506, if you increase the square footage of the entire living space by 1%, it will increase sale price by  ~$3,500. 
    
    B. Additionally, we recognize that many variables are interconnected and that many features need to be analyzed in the context with other factors. In particular, we believe that house size's relationship with home price also depends on the house's quality as measured by county's grading system. That a higher grade is associated with higher home price. Therefore, we recommend that home flippers take into consideration building quality. Details of the grading scale can be found here on [this website](https://info.kingcounty.gov/assessor/esales/Glossary.aspx?type=r). 
    
    C. Lastly, we recognize the various possibilities involved in flipping a house for profit and recommend adding bathrooms to increase sale price. For a house with an average price, one additional bathroom will increase sale price by  ~$31,000. 


## Next Steps

1. Calculate ratios of relevant interaction terms to put numbers into greater perspective. For example, bedroom to bathroom ratio or house size to lot size ratio. 

2. Find real estate data that includes other relevant information impacting house price. For example, kitchens and the presence of a pool. 

3. Obtain renovation cost in King County by house size for budget analysis 


## Additional Information

See the full analysis in the [Jupyter Notebook](https://www.google.com/) or review [this presentation](https://www.google.com/).

For additional info, contact

Eric Denbin: ericdenbin@gwu.edu

Allison Gao: allison.gao@nyu.edu

## Project Structure 

```## Project Structure

├── README.md
├── data      <-- CSV file used in analyses
├── images    <-- visualizations generated from working notebooks and external images
├── Individuals Notebooks       <--- Directory for individual workspaces
│   ├── allison
│   ├── eric
│   
│   
├── Final Notebook.ipynb    <-- Jupyter Notebook containing codes detailing project's analysis 
├── Non-technical Presentation.pdf   <-- non-technical presentation slides
└── .gitignore

