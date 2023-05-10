## Data Exploration
Following the youtube video: https://youtu.be/qfyynHBFOsM I created basic SQL queries in Microsoft SQL Server Management Studio. 
First we we edited the data in Excel. We edited two files CovidDeaths and CovidVaccinations. After that we Imported them in MSSMS. There were couple
of problems and I had to install Integration Services (SSIS) and  Microsoft ODBC Driver for SQL Server so that I could import the two datasets that I 
edited previously in Excel. I had to import the data using SQL Import and Export Wizard. After that I created queries following the video. Queries
were preparation for later visualizations in Tableau.The file named SQLQuery3.sql was created by me. To use the same file as instructor in Tableau I 
decided for further analysis file Tableau Portfolio Project SQL Queries.

* [SQL Queries](https://github.com/rokzupan1/portfolio-projects/blob/main/Data%20Exploration/SQLQuery3.sql)
* [Data](https://github.com/rokzupan1/portfolio-projects/blob/main/Data%20Exploration/CovidVaccinations.xlsx)
* [Data](https://github.com/rokzupan1/portfolio-projects/blob/main/Data%20Exploration/CovidDeaths.xlsx)
* [Theory about SQL language](https://github.com/rokzupan1/portfolio-projects/blob/main/Data%20Exploration/Building%20Blocks%20of%20Databases%20-%20Theory.txt)

## Tableau Visualization
Following the second video of this portfolio project: https://youtu.be/QILNlRvJlfQ we created visualizations in Tableau. 
Using the updated queries that were given in the description of the videos, I ran 4 queries and saved them as Excel File. The four tables had to be 
seperated, each in own file. Each on seperate sheet would not be sufficient. Then I imported them in Tableau Public and created 4 sheets following the video.
After that we created a simple dashboard containing all the 4 sheets. I learned some new things in Tableau and refresh my memory on things I learned before.
Here you can check the dashboard I created.

* [Dashboard](https://public.tableau.com/views/covid-deaths-vaccinations/Dashboard1?:language=en-US&:display_count=n&:origin=viz_share_link)
* [Edited SQL Queries](https://github.com/rokzupan1/portfolio-projects/blob/main/Tableau%20Visualization/Tableau%20Portfolio%20Project%20SQL%20Queries.sql)
* [Data](https://github.com/rokzupan1/portfolio-projects/blob/main/Tableau%20Visualization/Tableau%20Table%201.xlsx)
* [Data](https://github.com/rokzupan1/portfolio-projects/blob/main/Tableau%20Visualization/Tableau%20Table%202.xlsx)
* [Data](https://github.com/rokzupan1/portfolio-projects/blob/main/Tableau%20Visualization/Tableau%20Table%203.xlsx)
* [Data](https://github.com/rokzupan1/portfolio-projects/blob/main/Tableau%20Visualization/Tableau%20Table%204.xlsx)

## Data Cleaning
Following the third video of this portfolio project: https://youtu.be/8rO7ztF4NtU we've done some data cleaning. 
Using CONVERT we converted date format into a standardized form. We Populate Property Address Date. We then break out address into individual columns 
(address, city, state) - using two methods: SUBSTRING and PARSENAMES. After that we changed values with Y into Yes and N into No, so there were only 
two variants for SoldAsVacant. Then using CTE we removed duplicated, there were 104 duplicates. After that we deleted the unused columns that we modified earlier.

* [Data](https://github.com/rokzupan1/covid-deaths-vaccinations/blob/main/Nashville%20Housing%20Data%20for%20Data%20Cleaning.xlsx)
* [SQL Queries](https://github.com/rokzupan1/covid-deaths-vaccinations/blob/main/DataCleaning.sql)

## Correlation in Python
Following the fourth video of this portfolio project: https://youtu.be/iPYVYBtUTyE we've been figuring correlation between movies
specifications. We impoted tha packages and disabled the warning that pandas generates when you assign a new value to a slice of 
a DataFrame.  Then we imported the data and checked our data. We removed the missing values and check our data types of the columns.
We changed the data types of two columns and drop any duplicates. We than created a scatter plot that show correlation between budget
and gross earnings with plt() and with seaborn library. Using seaborn library we added the correlation line. Using the pearson method
we checked for any other major correlation and then we focused on plotted the correlation matrix to read the correlation easier.
Then we hypothesized that there is a major correlation between gross earnings and companies creating the movie. Using for loop we 
changed the all data type object into category type and then into numerical values of category. After that we created another correlation
matrix for numeric features again using the pearson method. Then we unstacked the correlation into one column and pick the high correlated
pairs and sorted them. Biggest take we can take from correlating this dataset is that there is a high correlation to gross earnings by 
votes and budget. 

* [Data](https://github.com/rokzupan1/portfolio-projects/blob/main/movies.csv)
* [Python Code](https://github.com/rokzupan1/portfolio-projects/blob/main/Movie_Correlation_Project.ipynb)

The Pearson correlation coefficient, Kendall rank correlation coefficient, and Spearman rank correlation coefficient are all measures of the degree of association or correlation between two variables. However, they differ in the types of data they are best suited for and the assumptions they make about the data.

Pearson correlation coefficient:
The Pearson correlation coefficient is used to measure the linear correlation between two continuous variables. It assumes that the data is normally distributed and that there is a linear relationship between the two variables. The Pearson correlation coefficient ranges from -1 to +1, where -1 indicates a perfect negative correlation, 0 indicates no correlation, and +1 indicates a perfect positive correlation.

Kendall rank correlation coefficient:
The Kendall rank correlation coefficient is a non-parametric measure of the degree of association between two variables. It measures the strength of the association between the two variables based on the ranks of the data, rather than the actual values of the data. It is often used when the data is not normally distributed or when there may be outliers. The Kendall rank correlation coefficient ranges from -1 to +1, where -1 indicates a perfect negative correlation, 0 indicates no correlation, and +1 indicates a perfect positive correlation.

Spearman rank correlation coefficient:
The Spearman rank correlation coefficient is also a non-parametric measure of the degree of association between two variables, similar to the Kendall rank correlation coefficient. However, it uses the actual values of the data, rather than the ranks of the data. It is often used when the data is not normally distributed or when there may be outliers. The Spearman rank correlation coefficient ranges from -1 to +1, where -1 indicates a perfect negative correlation, 0 indicates no correlation, and +1 indicates a perfect positive correlation.

In summary, the Pearson correlation coefficient is best suited for continuous data that is normally distributed, while the Kendall rank correlation coefficient and Spearman rank correlation coefficient are best suited for non-parametric data or data that is not normally distributed. The choice of which correlation coefficient to use depends on the type of data being analyzed and the assumptions that can be made about the data.

## Amazon Web Scraping Using Python
Following the fifth video of this portfolio project: https://youtu.be/HiOtQMcI5wg we were scraping data from amazon website and outport it as csv. We started by importing libraries and then connecting to the website where we got our data. After that we striped our queried data so it is easier to use. Using the today() function we added acolumn to our previous two columns of queried data. Then we saved this dataset in csv format. We then append our data that was the same as before so we got more rows of the same information. Then we define the check_review function that did all the steps previously described and using a while loop we checked if the review has changed every 3 seconds. If you stop the while loop after 24 seconds you will get additional 8 rows. This is an example how you can check number of reviews on Amazon product every 3 seconds.

* [Python Scraping](https://github.com/rokzupan1/portfolio-projects/blob/main/Amazon%20Web%20Scraper%20Project.ipynb)
* [Output Data](https://github.com/rokzupan1/portfolio-projects/blob/main/AmazonWebScraperDataset.csv)

## Automating Crypto Website API Pull Using Python
Following the preview video for the sixth video: https://youtu.be/2HfSFdPEFRg we signed up on coinmarketcap for use of public crypto APIs. We glanced the API documentation and copied the python code and changed the code to paste our API key in the code. With the ChatGPT help we jupyter changed the rate limit in Anaconda Prompt: lab --ServerApp.iopub_data_rate_limit=10000000. Usin pandas we then normalized data and put it in a dataframe. First we imported the 5000 rows but then we only focused on the top 15 rows.Then we created a function that did all the steps we did before and saved the values for 15 crpytocurrencies in a csv file. Then we created a foor loop that checks the values every 60 seconds. I left this loop run for 5 minutes and saved the values in a dataframe. We then grouped by our dataframe by name of the crypocurrencies and calculated the mean for change for 1h, 24h and some more values. We stacked the data and cleaned it that it looked a little better. Then we created a visualization that showed how did this 15 crpytocurrencies changed through different range of time. We than plotted the lineplot only for Bitcoin. 

* [Python Code](https://github.com/rokzupan1/portfolio-projects/blob/main/Automating%20Crypto%20Website%20API%20Pull%20Using%20Python.ipynb)
* [Output CSV](https://github.com/rokzupan1/portfolio-projects/blob/main/API.csv)

