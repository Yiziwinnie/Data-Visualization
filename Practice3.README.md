# Data-Visualization
**R &amp; Tableau**<br/>
<br/>
![picture1](https://user-images.githubusercontent.com/31257555/49932678-9cc66580-ff04-11e8-844d-bd54e8bb3c40.png)

> **Method: R**<br/>
In this problem, I did data manipulation first and then plotted them using geom_line().
I aggregated using aggregate (WL ~ Date, Water, mean), so I can get the water level in each day instead of in every hour.  In order to get a smooth curve, I set the different window size to get the best smooth curve. I gained the best output when the window size equal to 30 with fewer observations losing. As you can see that the different month is colored by different colors using 
geom_line(aes(color=factor(agg_data$month))). There is no unit of water level provided in raw dataset. The fake unit is used in my plotting. <br/>
**Analysis:**<br/>
It gives me the best view of the changes in the data when the window size is equal to 30. 
<br/>
<br/>

![picture2](https://user-images.githubusercontent.com/31257555/49932683-9df79280-ff04-11e8-82ec-9ddc190e7a52.png)<br/>
> **Method: R**<br/>
In this problem, I did data manipulate first and then plotted them using geom_tile(). I added new columns named month, date, day, and mon_abb. The tick markes are forced to represent in order by setting limit=c("Jan","Feb","Mar","Apr","May","Jun","Jul","Aug","Sep","Oct","Nov","Dec"). The leading 0s in day are moved by using %e. The color of water level in each day using scale_fill_gradient(low = "white", high = "steelblue"). 
<br/>
<br/>

<img width="738" alt="screen shot 2018-12-13 at 6 38 28 pm" src="https://user-images.githubusercontent.com/31257555/49933364-64278b80-ff06-11e8-9697-93270837f170.png">

<img width="674" alt="screen shot 2018-12-13 at 6 25 05 pm" src="https://user-images.githubusercontent.com/31257555/49932690-a223b000-ff04-11e8-84a3-18cfd73ffa6d.png">

> **Method: R**<br/>
I used treemap() and gained tree map with two subgroups.  I set the index index=c("company","division"), vSize="budget",type="value", and then set different colors of borders and labels, different size of borders, different positions of labels. The fun.aggregate = "sum" means that I aggregated value using sum function. I removed the legend because we can know the general information of budget based on the size and color of each division. In order to test the size and color is matched with real value or not, I aggerated the data and got the same results.  <br/><br/>
There are three problems that I need more time to figure out to improve the quality of my tree map. The position of title looks so wired. I double checked with the documentation of tree map, there is no way to change the location of title. However, there is no any problems when I exported image when I used the png("tree_map1.png") and dev.off(). The output is provided as above. I did not choose this way because the whole quality is worse than the previous one. The color of text in cell should be changed corresponding to the background color just we like Tableau does. Finally, it is better to display the sum of budget in each level. 
<br/>
<br/>

<img width="847" alt="screen shot 2018-12-13 at 6 25 32 pm" src="https://user-images.githubusercontent.com/31257555/49932693-a5b73700-ff04-11e8-809f-ec5af0bbeddc.png">
<img width="713" alt="screen shot 2018-12-13 at 6 25 51 pm" src="https://user-images.githubusercontent.com/31257555/49932695-a5b73700-ff04-11e8-9157-17e284408049.png">

> **Method: R**<br/>
I used all most the same method to get this tree map with two subgroups. The only different is I set the index index=c("company","division","office"), vSize="budget",type="index"(based on different categories), and add three more values in setting boarder color, the position of text, and the color of text, respectively. <br/>
There are two problems that I need more time to figure out to improve the quality of my tree map, just I mentioned previously.<br/>
**Analysis:**<br/>
There three main colors in my tree maps, the color of each division and the size of each office vary a little bit based on the value of budget. You can see three companies by looking the black boarders(size) and different color of within the black boarders(color), which is easier for people differentiate with appearance of colors. What’s more, we can look the general information of each division and each office by the same way. Yes, it is feasible with this dataset to communicate all three levels with a tree map. However, the information of the third level cannot communicate well compared with the other two levels. The difference of size and color is hard to differentiate in this level. 
