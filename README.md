# Multiple-Regression
Here, I am going to use acs_ny.csv dataset for various multiple regression models.
This dataset consists of variables which are not linear and they have a lot of data cleaning mistakes. I am trying to see if I can find those mistakes, and make a better model. So, there might be more than 10 models after I am finished. The R-squared values are around 0.3 which means Multiple Regression is not a good model. However, first I am going to try multiple regression to clean the data and get a sense out of the data and then in the future I will use other regression models. Peace!

Model 1: R-Square = 0.344
  Description: I designed my Model 1 to be a base model for all my other Models. I put every variable in the base model, and made dummy     variables for categorical variables recognized as objects in pandas DataFrame.
  I also did not delete any outliers.
  Note: My models where I started deleting outliers start from Model 6.

Model 2: R-Square = 0.291
  Description: I designed Model 2 using PCA and put every variable in the model. I made dummy variables from categorical variables and       standardized the variables too.
 
Model 3: R-Square = 0.344
  Description: I designed Model 3 from Model 1 trying to use Backward Elimination for the Multiple Regression. Since there were a lot of     variables, I used group Backward Elimination, meaning I took out all p-values containing 0.9 and above during the first elimination, 0-8   and above during the second elimination and so on. I put every variables at first, and took out the p-values more than 0.05.
  
Visualization Exercise with Matplotlib: This is when I visualized independent variables with the dependent variable to see how the data was distributed. The upcoming models are based on this visualization.
  
Model 4: R-square = 0.339
  Description: Using the Visualization Exercise with Matplotlib file, I got the idea of how the data was being distributed and I started     many tests to figure out which variables to delete and which to keep. I found out correlations between dependent vs independent           variables and dependent vs dependent variables to delete multi-collinearity and see which variables are linear to test assumptions of     multiple regression model.
  
Model 5: R-square = 0.258 - 0.322
  Description: For this model I used PCA(Principal Component Analysis) and FA(Factor Analysis) using both standardized and non-             standardized values using Model 4.
  
After building all these models, I decided it is time to deal with outliers and see the performance change. So, from Model 6 onwards, all the outliers are taken care of.

