  # STEPS THAT I TOOK ANALYZE WORLD HAPPINESS REPORT
  
  ## 1. Doing Imports, Data Preprocessing and checking for Missing Values  
  ![image](https://user-images.githubusercontent.com/78250442/232190300-4cc82976-2053-4732-8cd7-24b5de9ca629.png)  
  Output  
  ![image](https://user-images.githubusercontent.com/78250442/232190350-2748d3fa-2238-4939-bc91-d619f097d225.png)  
  In 2018 and 2019 certain data points were changed and therefore adding data for these years  
  ![image](https://user-images.githubusercontent.com/78250442/232190422-12ef9b26-859b-4ecc-b1f2-9d65f699b019.png)  
  Output  
  ![image](https://user-images.githubusercontent.com/78250442/232190457-2c4ccb8d-5202-4090-ad7d-bb3a0d17dee8.png)  
  Checking for Missing values  
  ![image](https://user-images.githubusercontent.com/78250442/232190502-5377efa0-a069-4b12-ac64-c66e149a7aaf.png)  
  ## 2. Time to understand Data  
   a) Shape of Data  
    ![image](https://user-images.githubusercontent.com/78250442/232190572-2527c08a-2258-4528-9e5d-651725c5ada0.png)
   b) Summary of stats  
    ![image](https://user-images.githubusercontent.com/78250442/232190609-86e22c56-ec36-4d06-a063-9754650048e4.png)  
    This trend cleary suggest that happiness is falling year by year with only 2019 being slighty more than 2019.  
  ## 3. Creating Factors and analyzing the difference between 2015 and 2019
  We first need to create a dataframe with the next columns:  
  Factor - our 7 factors
  Year - the years between 2015 and 2019
  Avg_value - average value of the factor for the year
  ![image](https://user-images.githubusercontent.com/78250442/232190775-008b9b43-eb69-4b6d-b19c-d2241f15bceb.png)  
  Output  
  ![image](https://user-images.githubusercontent.com/78250442/232190855-a82a0b5d-0f69-4272-804e-6a35d351ea98.png)  
  Graph    
  ![image](https://user-images.githubusercontent.com/78250442/232190904-72c62aa9-fac5-4e50-994a-8df5f3ff6957.png)
  
  ## Top 10 Most and least Happiest Countries  
  a) Avg top 10 countries
  ![image](https://user-images.githubusercontent.com/78250442/232191936-2c2ee4ff-7b10-46f2-a120-680ecb80871a.png)  
  Barchart  
  ![image](https://user-images.githubusercontent.com/78250442/232192068-790c9f9b-1881-407b-9996-0ad1c9b8ad97.png)  
  b) Least happy chart  
  ![image](https://user-images.githubusercontent.com/78250442/232192320-40ac0489-76ee-464a-b0dd-097ed6b063af.png)  
  Nothing surprising here either and goes in-line with the 7 factor study. Countries in war zones or with poor sanitation systems, diseases or very poor infrastructure are the least happy people out of all.
  
  ## 5. Observing the distribution  
  a) Distribution of Happiness Score  
  ![image](https://user-images.githubusercontent.com/78250442/232193163-32dd82b5-bb0c-422e-a95c-bf5822b07c32.png)  
  b) Distribution of other factors  
  ![image](https://user-images.githubusercontent.com/78250442/232193327-7466c12f-d493-4a81-841d-3893dea217c2.png)
![image](https://user-images.githubusercontent.com/78250442/232193341-21ec62bf-cb7a-4dd8-9d2c-4e772a26bb7c.png)

 ## 6. How factors influene happiness ( by Pearson Correlation )  
 ![image](https://user-images.githubusercontent.com/78250442/233239128-54dce297-ecdf-4fe9-9dc6-700b4fb6ef32.png)  
 Output  
 ![image](https://user-images.githubusercontent.com/78250442/233239574-5d0167b9-ea7e-4103-92c0-cdb9039b4e00.png)
  Creating a correlation matrix for better visualization  
  ![image](https://user-images.githubusercontent.com/78250442/233239765-cf338a6a-b082-46f3-ae96-83b62f35b298.png)
  Output  
 ![image](https://user-images.githubusercontent.com/78250442/233239844-ac767d2e-542b-427d-ada6-0d93d57aa39d.png)  
 It can be understood from the correlation matrix that GDP per captia (money) is the biggest determiner for the happiness score.    
 ## 7. Creating a model to predict Happiness Socre  
 a) Importing sklearn libraries and Models  
 ![image](https://user-images.githubusercontent.com/78250442/233240801-97367a1e-5080-40a2-a300-6b03ec798a9c.png)
 b) Creating data table, dependent variables, independent variables and train test model  
 ![image](https://user-images.githubusercontent.com/78250442/233240932-aa47d624-0ceb-45e7-8a43-09e93815b9eb.png)  
 c) Creating a function to test the models and then comparing MAE's(Mean Average Error)  
 ![image](https://user-images.githubusercontent.com/78250442/233241381-4670bb95-6998-4311-9d90-1afce8c60135.png)  
 d) Running Models  
    i) Linear Regression  
    ![image](https://user-images.githubusercontent.com/78250442/233241629-81293345-b878-4487-9fbc-93978f5951c0.png)  
    ii) Random Forest Regressor  
    ![image](https://user-images.githubusercontent.com/78250442/233241734-c62256b7-24ba-47d4-b8f9-a4ba31586e98.png)  
    iii) Decision Tree  
    ![image](https://user-images.githubusercontent.com/78250442/233241866-4817846e-cfaa-40a7-a761-2858c28d8f22.png)  
    iv) Bayesian Linear Model  
    ![image](https://user-images.githubusercontent.com/78250442/233241968-30806ede-559c-4f6f-ba61-21e6e24cd37a.png)  
    v) Lasso Lars  
    ![image](https://user-images.githubusercontent.com/78250442/233242094-44c4c0f6-92fe-424e-8a62-ba49b4374d98.png)  
   Linear Regression and the Bayesian Ridge were the models that performed the best (they had the smallest mae out of all).  
   Selecting Bayesian as the final model  
   ![image](https://user-images.githubusercontent.com/78250442/233242349-97a095e0-e0ea-42e2-a333-e8604baa51ba.png)





 


  
