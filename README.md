**Introduction**

This README describes work done on the Spaceship Titanic data set. Resources used include Python and associated packages Jupyter, matplotlib, Seaborn and scikit-learn. These packages all come as part of the Anaconda distribution of Python.
The analysis takes the form of a single Jupyter notebook of filename given above. To view this file, download it from this repository and start Jupyter notebook in the folder containing the file. Use the command Jupyter notebook on the command line.
Alternatively, view a static version of the notebook (by providing its GitHub url) using Jupyter Nbviewer.
The Spaceship titanic dataset is available on Kaggle. To gain access to the dataset, visit this link https://www.kaggle.com/competitions/spaceship-titanic and download the dataset to your local machine. The zip file contains 3 file. The train dataset, test dataset and a sample submission dataset.
All images intended for inclusion in this README are located in the images subdirectory of this repository.
Spaceship Titanic
The dataset used for this project is the Spacehip Titanic dataset, gotten from Kaggle. It describes an interstellar passenger liner with almost 13,000 passengers on board, The vessel set out on its maiden voyage, transporting emigrants from our solar system to three newly habitable exoplanets orbiting nearby stars.
While rounding Alpha Centauri en route to its first destination—the torrid 55 Cancri E—the unwary Spaceship Titanic collided with a spacetime anomaly hidden within a dust cloud. Sadly, it met a similar fate as its namesake from 1000 years before. Though the ship stayed intact, almost half of the passengers were transported to an alternate dimension.
The goal of this project is to help predict which passengers were transported by the anomaly using records recovered from the spaceship’s damaged computer system.

**Descriptive Statistics**

I used the shape method in pandas to check the shape of both datasets and the training data set contains 8693 rolls and 14 columns while the test dataset contains 4277 rolls and 13 columns.
Checking more information about the dataset, I used the info() method in pandas which shows more information about the columns in the datasets. The dataset had a lot of missing data for both the categorical and numerical columns which we will handle in a moment and the train dataset contains a target column called “Transported”(The column we are trying to predict), while the test dataset does not.
I used seaborn’s heatmap to get a visual of all missing data in each column of our train dataset and only the PassengerID and Transported columns do not have missing data.
Pandas describe() can provide a quick summary of the numerical columns in the data set as outlined in the notebook. From this summary, we can say that
1.	The Average age on the ship is 28 years old.
2.	The minimum age on the ship is 0 which can mean we have babies on the ship.
3.	The oldest age on the ship is 79 years old.
   
Data Cleaning - Handling missing values
Cryosleep - Plotting a bar plot of Cryosleep on the X axis and Foodcourt on the Y axis we can see all users in cryoSleep spent 0 in foodcourt. To fill the missing data, we are going to create a function that will return False for Cryosleep if Food Court is zero and return true if otherwise.
HomePlanet, VIP - From our dataset, No one from earth was in the VIP on the ship, This information helped me  to handle the missing values for both Home planet and VIP.
Age – To handle the missing values in the age column, we used the mean of all passengers in the Homeplanet column to fill the missing values.
RoomService,  ShoppingMall, Spa, VRDeck – I used the mode of the distribution in these columns to fill in the missing values in these columns.
**Note**: Data cleaning process for all other columns are similar and shown in the code.

**Technologies used**
Python
Jupyter, Pandas
Seaborn, Matplotlib
Sklearn


