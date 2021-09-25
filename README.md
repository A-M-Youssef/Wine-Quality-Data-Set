# Wine Quality DataSet
There are two datasets that provide information on samples of red and white variants of the Portuguese "Vinho Verde" wine.</br>
Each sample of wine was rated for quality by wine experts and examined with physicochemical tests.</br>
Due to privacy and logistic issues, only data on these physicochemical properties and quality ratings are available (e.g. there is no data about grape types, wine brand, wine selling price, etc.)</br>
</br>
**Attributes in Each Dataset:**
</br>
##	Physicochemical Properties

### 1)	Fixed Acidity
### 2)	Volatile Acidity
### 3)	Citric Acid
### 4)	Residual Sugar
### 5)	Chlorides
### 6)	Free Sulfur Dioxide
### 7)	Total Sulfur Dioxide
### 8)	Density
### 9)	pH
### 10)	Sulphates
### 11)	Alcohol

##	Quality Rating
### 12)	Quality - Score between 0 and 10 (median of at least 3 evaluations made by wine experts)</br>
</br> 

**In the notebook below, I investigate several questions about this data using statistics and plots.**</br>
</br>

## Q1: which of the following variables (Volatile Acidity, Residual Sugar, pH, and Alcohol) is most likely to have a positive impact on quality?
For this question, I will plot several scatter plots and deduce the correlation.

## Q2: Is a certain type of wine (red or white) associated with higher quality?
For this question, I compared the average quality of red wine with the average quality of white wine with groupby. 

## Q3: What level of acidity (pH value) receives the highest average rating?
This question is more tricky because unlike color, which has clear categories you can group by (red and white) pH is a quantitative variable without clear categories. However, there is a simple fix to this. I created a categorical variable from a quantitative variable by creating my own categories. So, I created a new column called acidity_levels with these categories:
</br>
Acidity Levels:</br>
High: Lowest 25% of pH values</br>
Moderately High: 25% - 50% of pH values</br>
Medium: 50% - 75% of pH values</br>
Low: 75% - max pH value</br>
Here, the data is being split at the 25th, 50th, and 75th percentile.
</br>

## Q4: Do wines with higher alcoholic content receive better ratings?
To answer this question, I used query to create two groups of wine samples:</br>

Low alcohol (samples with an alcohol content less than the median)</br>
High alcohol (samples with an alcohol content greater than or equal to the median)</br>
Then, find the mean quality rating of each group.</br>

## Q5: Do sweeter wines (more residual sugar) receive better ratings?
Similarly, I used the median to split the samples into two groups by residual sugar and find the mean quality rating of each group.
