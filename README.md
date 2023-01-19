# Data Science Pipeline Project

The goal of my project is to work with an automobile dataset to predict the price of the automobile. 
The data used includes information about various features of the automobile. 

The dataset colums:
1. symbolling: 			  -3, -2, -1, 0, 1, 2, 3.
2. normalized-losses: continuous from 65 to 256.
3. make:			      	alfa-Romero, Audi, BMW, Chevrolet, dodge, honda,
  			          		Isuzu, Jaguar, Mazda, Mercedes-Benz, mercury,
 					            Mitsubishi, Nissan, Peugeot, Plymouth, Porsche,
  					          Renault, Saab, Subaru, Toyota, Volkswagen, Volvo
4. fuel-type:  				diesel, gas.
5. aspiration: 				std, turbo.
6. num-of-doors: 			four, two.
7. body-style:  			hardtop, wagon, sedan, hatchback, convertible.
8. drive-wheels:    	4wd, fwd, rwd.
9. engine-location: 	front, rear
10. wheel-base: 			continuous from 86.6 120.9.
11. length: 		   		continuous from 141.1 to 208.1.
12. width: 		    		continuous from 60.3 to 72.3.
13. height:			     	continuous from 47.8 to 59.8.
14. curb-weight: 			continuous from 1488 to 4066.
15. engine-type:			DOHC, dohcv, l, ohc, ohcf, ohcv, rotor.
16. num-of-cylinders:			eight, five, four, six, three, twelve, two.
17. engine size: 			continuous from 61 to 326.
18. fuel-system: 			1bbl, 2bbl, 4bbl, idi, mfi, mpfi, spdi, spfi.
19. bore: 			    	continuous from 2.54 to 3.94.
20. stroke:				    continuous from 2.07 to 4.17.
21. compression-ratio:			continuous from 7 to 23.
22. horsepower:		   	continuous from 48 to 288.
23. peak-rpm: 				continuous from 4150 to 6600.
24. city-mpg:			   	continuous from 13 to 49.
25. highway-mpg:			continuous from 16 to 54.
26. price: 				    continuous from 5118 to 45400.

*Exploratory Data Analysis*
- Data preprocessing is a data mining technique that's used to take raw data and put it in a useful formatting. Exploratory data analysis is an approach of analyzing data sets to summarize their main characteristics. In this section I checked the data column's name, dataset shape, and dataset info - printing the 5-point summary of the dataset using the df describe command. 

*Missing Value Handling*
- This is where the data was cleaned. If a column had a question mark it meant it was missing a value. I dealt with this by making them null values and followed this by filling them with the most repeated value of the column. After doing this it meant I could make the distribtion graph of the price, shown below.
<img width="362" alt="image" src="https://user-images.githubusercontent.com/56044999/207619970-28bfd5b3-c6b6-4c7c-855c-28d0346ffcc8.png">
- Following this, the value count of the make column was checked and with it I created a column with all of that data. I used this to create a bar graph with the mar makes on the x axis and pricing on the y.
<img width="412" alt="image" src="https://user-images.githubusercontent.com/56044999/207620717-69b82e97-d36a-47fb-b5b4-01866eb50ede.png">

*Label Encoding*
- Label encoding is a process in which non-numeric items are converted to the numeric form so they become machine-readable.  

*Scatter Plot an Distribution Graph*
- Scatter plots help see if there are linear relationships. The scatter plot made was of each column with the price column. 
- Scatter plots help see if there are linear relationships. The scatter plot made was of each column with the price column. 
<img width="468" alt="image" src="https://user-images.githubusercontent.com/56044999/207623240-e4f95fbc-335b-46fe-bde4-60ad6d543f40.png">
<img width="468" alt="image" src="https://user-images.githubusercontent.com/56044999/207623544-6875ac02-20ab-47b3-adf9-4e38e5ad2461.png">

*Standardizarion*
- Standardization is a technique where you make the data scale-free by converting the distribution of data into the following: mean - zero, sd - 1
- The StandardScaler class from sklearn's preprocessing module is used, calling fit_transform() and passing it into our pandas dataframe.

*Random Forest*
- Random Forest Regression is a supervised learning algorithm that uses ensemble learning method for regression. It combines predictions from multiple ML algorithms to make a better prediction than just one model.
- A grid search CV technique is used to get the best parameters for the model. After fitting the model, I then printed the explained variance score, mean squared error, and r2 score for testing the dataset.
