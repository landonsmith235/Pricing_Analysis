![alt text](https://github.com/landonsmith235/Pricing_Analysis/blob/27691e35af9dd44a0f9c81941ffbff6ded094fe4/Images/pricing_title_slide.jpg)

## **Overview**
Due to rampant inflation in a post-COVID-19 pandemic world, the cost of red meat-based inventory for steakhouses has increased dramatically in a condensed amount of time. To cope with the higher cost of inventory, the Dal Rae has been forced to make trade-offs that customers may view as detrimental to their business in order to maintain the same level of profitability post-COVID-19, including implementing a reduction in portion sizes, an increase in menu prices, and a reduction of staff. The goal of this project is to ensure that the Dal Rae’s red meat entrées maintain a target contribution margin of 75% while making the trade-offs that are optimal in terms of customer sentiment. To achieve this goal, we performed secondary research, where we consulted with management to identify attributes about their customer base, and primary research, which came in the form of a survey circulated to customers. We utilized Ward's Agglomerative Clustering to determine customer tolerance for the various trade-offs being proposed and used survey results pertaining to dining frequency in tandem with Point of Sale system data to predict the price elasticity of the Dal Rae's red meat offerings. After synthesizing all of our findings together, our final recommendation for the restaurant was to decrease the portion size of its "Dal Rae Famous Pepper Steak" from 12 oz to 10 oz while maintaining a price of $69.50.

## **Technologies Utilized**
* R Studio
* Excel
* Google Forms

## **R Studio Libraries**
* dplyr
* ggplot2
* readxl

## **Relevant Repository Contents & Descriptions**

### **Presentation Folder**
This folder contains a Microsoft PowerPoint presentation that provides an overview of the methodologies utilized throughout the project.

### **Code Folder**
This folder contains all of the code utilized to perform our analysis. You can find a description of each file below:

#### **Dal Rae Popular Items.Rmd**
In this file, we determined the top red meat-based entrees within the Low (<$30), Medium ($30-$40), and High (>$50) price ranges. Our results were the Poor Man's Pepper Steak, the Medallions of Filet Mignon, and the Dal Rae Famous Pepper Steak for each category respectively.

#### **Dal Rae Sensitivity Cluster Analysis.Rmd**
In this file, we used Ward's Agglomerative Clustering in order to differentiate different segments of the customer base by trade-off preference. We determined that there were four main groups of customers:
* a group that was intolerant of a downgrade in ingredients but moderately tolerant of all other trade-offs
* a group that was moderately tolerant of price adjustments but intolerant of all other trade-offs
* a group that was apathetic to any trade-offs implemented
* a group that was intolerant of the removal of sides, removal of low contribution margin menu items, and a downgrade of ingredients but moderately accepting of all other trade-offs
Overall, the trade-off that customers were least sensitive to was price adjustment, a finding that was consistent with our initial hypothesis.

#### **Dal Rae Elasticity & Demand Curve Analysis.Rmd**
In this file, we calculate the total number of entrées sold at each price point and remove price points with extremely low volume and menu bundles. We then compute the average number of entrées that were sold per day and use this new metric, which accounts for the variable of duration of time on the menu, to represent our quantity. We can then calculate the price elasticity of each menu item using the newly defined quantity, on both the data collected from our customer survey and Point of Sale system data. In this case, our survey data showcased much higher price elasticity than the actual POS data, suggesting that customers' answers on surveys don't always align with their actions. After calculating our elasticities, we constructed demand curves to visualize the expected quantity sold at different price points.
