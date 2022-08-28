Ramen Exploratory Analysis
### Objective
The project intent to do Exploratory Analysis of Ramen dataset. The attempt is to draw and analyse different patterns in the dataset that can give insights in the Ramen Noodles industry.

### 🔗Repository
| File     | Description                |
| :------- | :------------------------- |
| ramen-exploratory-analysis.ipynb | ramen analysis Jupyter Notebook code|
| ramen-ratings.csv | ramen analysis Jupyter Notebook code|

### Roadmap
- Averge Stars by Countries
- US and Japan Comparision
- Number of Countries where each brand is eaten
- Top Ramens of 2016
- spicy Ramen
- Star differences for different style 

### Library
- numpy for linear algebra functions
- pandas for data processing 
- matplotlib for data visualization

### Dataset
The dataset has coloumns Review# (review number), Brand, Variety, Style, Country, Stars and Top Ten, whose datatype information is found out using .info method. 

![](https://github.com/Shriyamkgp/ramen_analysis/blob/09d27a1de4fa57c65498cf0714b515dda3ed65e1/Media/2'.png)

#### Average Stars by Countries
In this section we group ramen noodles on the country basis and then take mean of the stars given for each country. The returned sequence is converted to DataFrame format for sorting.
The data is ploted to horizontal barchart using matplotlib library(refer to code)

![](https://github.com/Shriyamkgp/ramen_analysis/blob/09d27a1de4fa57c65498cf0714b515dda3ed65e1/Media/3'.png)


#### Comparision between Japan and US
Here I extract from given dataframe, entries whose country value is Japan and USA and then save them into two seperate new dataframes. Then find mean value of stars for different companies operating in Japan and USA. The method used is grouping (dataframe.groupby) the company specific dataframes on by companies and finding the mean value. Finally we plot bar graph comparing average ratings of a company in Japan and US. 

![](https://github.com/Shriyamkgp/ramen_analysis/blob/09d27a1de4fa57c65498cf0714b515dda3ed65e1/Media/5'.png)


#### Counting number of countries where a brand is Eaten.
Here I start with grouping values by their country and brand, thus to recive a dataframe which looks like..

![](https://github.com/Shriyamkgp/ramen_analysis/blob/6b6ef49b2e1c063b025cda25c8242e2f47b8a631/Media/5''.png)

Then save this as datafame and use groupby method for brand to count the country (refer to code file). Finally we create a bar plot for the value by using matplotlib.

![](https://github.com/Shriyamkgp/ramen_analysis/blob/09d27a1de4fa57c65498cf0714b515dda3ed65e1/Media/6.png)

#### Top Ramen of 2016
In this section I find top rated ramen from the given dataset in year 2020. In first step I found unique values in 'Top Ten' using .unique() method. Then we extract the rows from the dataframe which has substrig "2016" present. 

![](https://github.com/Shriyamkgp/ramen_analysis/blob/6b6ef49b2e1c063b025cda25c8242e2f47b8a631/Media/12.png)

![](https://github.com/Shriyamkgp/ramen_analysis/blob/6b6ef49b2e1c063b025cda25c8242e2f47b8a631/Media/13.png)

#### spicy Ramen
Here I create a new dataframe named Ramen_spicy by extracting the rows where spicy|Spicy sub-string is present in Variety column. This dataframe is specifically for spicy ramen. Next In this new dataframe, group by country and count the number of stars under each group. The counted number represent figure of number of people eating spicy ramen in each country. The the new dataframe is named Ramen_spicy_country, which is sorted and saved as dataframe Ramen_spicy_country_10 for the ease of understanding. We repeat the same process to find out the number of people rating ramen for each country and take top 10 values in Ramen_country_10 dataframe. Finally we plot both the dataframes for comparision.

![](https://github.com/Shriyamkgp/ramen_analysis/blob/6b6ef49b2e1c063b025cda25c8242e2f47b8a631/Media/14.png)

![](https://github.com/Shriyamkgp/ramen_analysis/blob/6b6ef49b2e1c063b025cda25c8242e2f47b8a631/Media/16.png)

#### Star differences for different style
I imported seaborn in this section to use it's categorical plot feature. The final graph have been ploted for dataframe Ramen and dataframe Ramen_Nissin (shown).

![](https://github.com/Shriyamkgp/ramen_analysis/blob/6b6ef49b2e1c063b025cda25c8242e2f47b8a631/Media/18.png)
