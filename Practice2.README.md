# Data-Visualization
R &amp; Tableau
![picture1](https://user-images.githubusercontent.com/31257555/49928364-fa55b480-fefa-11e8-81e3-e5a6b66333af.png)
> **Figure 1.**<br/>
**Method: R**<br/>
I added a new column named Error and absulutError based on basic calculation. I used  geom_violin() and geom_boxplot() to plot x= Test, y= absoluteError and set the color= Test without legend. And then I sorted value by median absolute error and bolded and center the title. What’s more, the x labels were shortened.<br/>
**Analysis:**<br/>
It is harder for people to measure the difference of Color Value and Slope based on their median absolute error which are equate to 0.2, showing higher than the rest of test type. It is slight harder for people to measure volume based on the median of absolute error is equal to 0.15. The difficulty level of measuring the difference of angle, area, and vertical unaligned distance are almost the same if we only take on their median which are equal to 0.1. It is easier for people to measure the difference of unaligned length and aligned vertical distance showing their median of absolute error are 0.07 and 0.05, respectively. 
We can look the curve of violin to see how data distributes in each test. The peak of curve stands for more people will make mistake with specific absolute error value. This extra information is represented by boxplot individually. <br/>
For aligned vertical distance, thee peaks occur. There are three ranges that people will mistake in different level. Most people will not make mistake, some people make mistake which presents absolute error value with 0.07, few people make mistake which presents absolute error value with 0.1, the rest of them will make mistake with different error. For unaligned length, many people make mistake which presents absolute error value with 0.05, some people make mistake which presents absolute error value with 0.1, few people make mistake which represents other range of absolute error. The median error will occur in the middle of two symmetric peaks of violin or occur at the peak of curve when there are two asymmetric peaks or only one peak. <br/>
There are three noticeable clumping of response for aligned vertical distance, two noticeable clumping in unaligned length, two noticeable clumping in angle, two noticeable clumping in area, two noticeable clumping in unaligned vertical distance, three noticeable clumping in volume, two noticeable in color value, and two noticeable clumping in slope. <br/>
<br/>
<br/>

![picture2](https://user-images.githubusercontent.com/31257555/49928365-faee4b00-fefa-11e8-9382-10db43168397.png)
> **Figure 2.**<br/>
**Method: R**<br/>
I used geom_violin() and geom_boxplot() to plot x= Test, y= Error and set the color= Test without legend. And then I sorted error value by median and bolded and center the title. What’s more, the x labels were shortened.<br/>
**Analysis:**<br/>
Based on looking at the median value of error, we can see that the tests of color value, unaligned length, angle, unaligned vertical distance are generally underestimated by people. The tests of area, volume and slope are generally overestimated by people. I used the error and test to graph this test. I have to mention that the absolute error can’t be used to get this result because it cannot differentiate the overestimation and underestimation. The violin and boxplot could reveal this clearly as you see on the graph as above. If the value of error is negative standing for underestimation and the value of error is positive standing of overestimation. What’s more, we can see some peaks in each test. It means that more people will make that specific error with different value of error.  <br/>
<br/>
<br/>

![picture3](https://user-images.githubusercontent.com/31257555/49928378-fe81d200-fefa-11e8-864b-8aabe62292a6.png)
> **Figure 3.**<br/>
**Method: R**<br/>
First, I subset the data to get subjects 56 to 73 using [student$Subject >=56 & student$Subject<=73,] and reset the value of Display using Subjects$Display[Subjects$Display== 1] <- "Display1" and Subjects$Display[Subjects$Display== 2] <- "Display2". And I also used geom_violin() in my graph. <br/>
**Analysis:**<br/>
Yes, there is some differences in the values for Display 1 and 2
As you can see as above, for trial B, the peak of Display1 marked in red is about -0.15 while peak of Display2 marked in blue is about 0. It means that people participants get better at judging after having done trial B once. For trial C, the peak of Display1 marked in red is about -0.13 while peak of Display2 marked in blue is about 0. It means that people participants get better at judging after having done trial C once. For trial D, the peak of Display1 marked in red is 0,0.1, and 0.2, respectively, while peak of Display2 marked in blue is about 0. 
We can see that blue curve spread wider than the red curve. It means that people participants do not get better at judging after having done trial D once, the result even gets worse.<br/>
<br/>
<br/>

**Figure 4: R**<br/>
![picture4](https://user-images.githubusercontent.com/31257555/49928379-ff1a6880-fefa-11e8-906c-230fd72ca284.png)<br/>
**Figure 5: Tableau**<br/>
![picture5](https://user-images.githubusercontent.com/31257555/49928380-ffb2ff00-fefa-11e8-8608-7545edf996af.png)

> **Method: R & Tableau**<br/>
First, I used Tableau(filter Test: Vertical distance, non- aligned) to find those abnormal points and found the corresponding subjects and then used R to highlight those points in orange. After that, I reset the value of Display using Subjects$Display[Subjects$Display== 1] <- "Display1" and Subjects$Display[Subjects$Display== 2] <- "Display2" , get the first subset data using subset(student, Test=='Vertical Distance, Non-Aligned') , and get the second subset data using data[data$Subject %in% c(56:68,54,71,73) & data$Test=='Vertical Distance, Non-Aligned' & data$Display=='Display1'& data$Response==1,] , and finally set x= Subject, y= Response and bolded and centered the title. <br/>
**Analysis:**<br/>
Abnormal points: Subject 54,56, 57, 58,59,60,61,62,63,64,65,66,67,71,73 
All true values gave by those responses are 1, no matter the trial is B, C, and D for Display 1.  
<br/>
<br/>

**Figure 6. Subjects: 56-73**<br/>
![picture6](https://user-images.githubusercontent.com/31257555/49928390-03468600-fefb-11e8-8f41-2b5e8856b8fd.png)

**Figure 7. All subjects**<br/>
![picture7](https://user-images.githubusercontent.com/31257555/49928392-03468600-fefb-11e8-92e1-07064cce20c7.png)
>**Method: R**<br/>
I used geom_split_violin () which is a function I searched online and geom_boxplot() to plot x= Trial, y= absulteError and set the color= Trial with legend. There are two data sets I used, one is the whole dataset, another one is the subset of dataset (subjects: 56-73) using Subjects=student[student$Subject >=56 & student$Subject<=73,]. And then I bolded and center the title.<br/>
**Analysis:**<br/>
Those two graphs diver the information that a little bit different from that of 4c. does. I used the absolute error here. Generally, we can say that participants do get better at judging after having done trial once no matter from some of participants or all participants. The way we look at the curve should focus on the height and location of their peaks. 
(I use absolute error instead of error and used distinct way, geom_split_violin (), to meet the requirement, and the information I gained from this way is different from the result shown previously)
<br/>
<br/>

**Figure 8. Daily adjusted Closing Price**<br/>
![picture8](https://user-images.githubusercontent.com/31257555/49928394-03df1c80-fefb-11e8-96c5-d7a67232cd93.png)

**Figure 9. Average adjusted Closing Price by Year**<br/>
![picture9](https://user-images.githubusercontent.com/31257555/49928396-03df1c80-fefb-11e8-99f2-7cd9a4f1a966.png)

>**Method: Tableau**<br/>
Daily adjusted Closing Price<br/>
I used Tableau to answer this question. I set the x= Year (Using Exact Date), y= Adjust Close Price, size = Volume (SUM). The range of y is set fixed value from 0 to 60 and added dollar sign with value in y axis.  The range of year is from 1990 to 2001 which is corresponding to the raw data. Because it shows daily price, so I did not choose any aggregation methods.  However, it is difficult to see the daily price because there are too many data. It is hard to get extra information when I set the Volume measure to alter the thick along the curve. It looks wired that  it event has some circles showing on the graph.  That’s why I display the second graph. <br/><br/>
Average adjusted Closing Price by Year<br/>
I set the x= Year (Using Year), y= Adjust Close Price(AVG) & y= Adjust Close Price(AVG), size = Volume(SUM). What’s more I used the dual axis for plotting the line marked in blue and plotting the scatter plot marked in orange. The range of y is I should set up to 50, however, there is an issue that I can’t figure out. That’s why I highlighted the minimum and maximum value of closing price. The range of year is from 1990 to 2000 because we use the average instead of daily price. I also set a reference lined named average price (setting computation and value) and added dollar sign with value in y axis.  Now we can easier see the change of volume by seeing the thickness of line compared with the daily graph. I have to say the result is better, but this is not the best way to display, I will show in following answer. 
<br/>
<br/>

![picture10](https://user-images.githubusercontent.com/31257555/49928386-02adef80-fefb-11e8-88e0-474241e437ea.png)
>**Figure 10.**<br/>
**Method: Tableau**<br/>
I set the x= Year (Using Year), y= Adjust Close Price(AVG) & y= Adjust Close Price(AVG), color = Volume(SUM). What’s more I used the dual axis for plotting the line marked in graduated color (Break= 5) and plotting the scatter plot marked with black border. The range of y is I should set up to 50, however, there is an issue that I can’t figure out. That’s why I highlighted the minimum and maximum value of closing price. The range of year is from 1990 to 2000 because we use the average instead of daily price. I also set a reference lined named average price (setting computation and value) and added dollar sign with value in y axis.  Now we can easier see the change of volume by seeing the changing color of line compared with the daily graph. 
<br/>
<br/>

![picture11](https://user-images.githubusercontent.com/31257555/49928387-02adef80-fefb-11e8-8eed-ddd2aebd6a8a.png)
>**Figure 11.**<br/>
**Method: Tableau**<br/>
This time, I used Volume measure to alter both color and size and got the graph as above. The method is similar with that of 5b.<br/>
**Analysis:**<br/>
It is hard for us to see the change of volume based on the thickness of line, not very noticeable. In my opinion, using the Volume measure to alter the color of the line at each point communicates the Volume data more efficiently. What’s more, combining two methods, size and color, may more efficient than that of only using color. 
<br/>
<br/>

![picture12](https://user-images.githubusercontent.com/31257555/49928389-03468600-fefb-11e8-97ec-167e40c88fc7.png)
>**Figure 12.**<br/>
**Method: Tableau**<br/>
I set the x= Year (Using Year), y= Adjust Close Price(AVG) & y= Adjust Close Price(AVG), color and size = Volume(SUM). What’s more I used the dual axis for plotting the line marked in graduated color (Break= 5) and plotting the scatter plot marked with black border. I highlighted the minimum and maximum value of closing price and added dollar sign with value in y axis. There is a difference between this graph and the graph I displaed as above. The y-axis is set log10. I selected scales as Logarithmic and position. The line will not show in 1990 because the value of 1990 is less than 1, so I edited the axis and selected Symmetric and the value of 1990 shows up. To let audience clearly understand of the scale of y-axis, I added the subtitle to state that this is logarithmic scale value labeled as [log10]. I tried to use log2(Using Log([Adjust.Close], 2]) )to see how does the line look like, provided as below for your reference. The shape is the same. Since we will use the natural log in 5e, so I choose using log 10 here. <br/>
**Analysis:**<br/>
This line is not very steep compared with the previous one without using log10. It looks like a straight line with a smaller slope rate. It means that the closing price has kept stable increasing, not change dramatically, along the year.
![picture13](https://user-images.githubusercontent.com/31257555/49928391-03468600-fefb-11e8-8375-08224a761d84.png)
<br/>
<br/>

**Figure 13. By month**<br/>
![picture14](https://user-images.githubusercontent.com/31257555/49928393-03df1c80-fefb-11e8-892c-4ded97bf9f1e.png)

**Figure 14. By quarter**<br/>
![picture15](https://user-images.githubusercontent.com/31257555/49928395-03df1c80-fefb-11e8-9917-2f5438a81de9.png)
>**Method: Tableau**<br/>
The method I used for this answer is almost same with the method of 5d. There are two differences between those two graphs and the graph showing in 5d.  I created a new column named In(price) which is natural log of adjusted closing price. I selected x = month and quarter, respectively, y=In(Price)(AVG). That’s why you can see there are more circles showing in the graph by month than that of by quarter. To let audience clearly understand of the scale of y-axis, I added the subtitle to state that this wise percentage labeled as Price increase % with as [Natural log].  <br/>
**Analysis:**<br/> 
There are 15 points that are between 15% and 20% increases in my graph by month. There are 5 points that are between 15 and 20% increases in my graph by quarter. Because we are supposed to identify three surges in price, I choose to answer this question my graph by month. Those three surges occur on July,1995, November 1995, and June,1996. 
![picture16](https://user-images.githubusercontent.com/31257555/49928397-03df1c80-fefb-11e8-8f92-481af69d49a0.png)
<br/>
<br/>

![picture17](https://user-images.githubusercontent.com/31257555/49928409-093c6700-fefb-11e8-91da-a6af85b96f2b.png)
> **Figure 15.**<br/>
**Method: Tableau**<br/>
The method I used for this answer is almost same with the method of 5e. There is only one difference between this graph and the graph showing in 5e. I selected x = data (Using year).<br/>
**Analysis:**<br/> 
I keep using the natural log because this question asks me to identify the point that yearly % wise changes fastest. The point in 2000 changes fast because it is located between 35% and 40% increase. 
<br/>
<br/>

![picture18](https://user-images.githubusercontent.com/31257555/49928410-09d4fd80-fefb-11e8-8256-5c834334d867.png)
> **Figure 16.**<br/>
**Method: Tableau**<br/>
I set the x= Year (Using Year), y= Adjust Close Price(AVG) & y= Adjust Close Price(AVG), size = Volume(SUM). What’s more I used the dual axis for plotting the line marked in blue and plotting the scatter plot marked in orange. The range of y is I should set up to 50, however, there is an issue that I can’t figure out. That’s why I highlighted the minimum and maximum value of closing price. The range of year is from 1990 to 2000 because we use the average instead of daily price. I also set a reference lined named average price (setting computation and value) and added dollar sign with value in y axis. This graph shows in 5a.as well.<br/>
**Analysis:**<br/> 
Yes, it works better when the curve has fewer data points because I can see there are less volume in 2000 compared with the rest of years. This information cannot get previously because too much data point may also cause the thickness of the curve. 
<br/>
<br/>

![picture19](https://user-images.githubusercontent.com/31257555/49928412-09d4fd80-fefb-11e8-8304-52a2809b5c19.png)
> **Figure 17.**<br/>
**Method: Tableau**<br/>
I set the x=Messier Number, y= Distance_LY, color = Season. The range of y is set fixed value from 0 to 110 and the range of x is set using log10. To let audience clearly understand of the scale of y-axis, I added the subtitle to state that this is logarithmic scale value labeled as [log10]. I kept the x not changed and tried putting the rest of variables into y one by one and colored them using categorical variables. I removed Null from my graph. <br/>
**Analysis:**<br/>
As you can see, objects marked in red standing for Su season having smaller messier number, mainly ranging from 0 to 30. Objects marked in green standing for Wi season having the moderate number, ranging from 30 to 50. Objects marked in orange standing for Sp season having larger messier number, mainly ranging from 50 to 70 and from 80 to 110. Objects marked in blue standing for Au season having small messier number, mainly ranging from 30 to 35. What’s more, it also shows that the messier objects located far away distance are more likely to have large messier number.
<br/>
<br/>

![picture20](https://user-images.githubusercontent.com/31257555/49928413-0a6d9400-fefb-11e8-8109-7761486c8d7a.png)
> **Figure 18.**<br/>
**Method: R**<br/>
I used geom_boxplot(),geom_point(), and geom_jitter()  to plot this graph. The null value is removed by using ggplot(data=subset(Messier, !is.na(Kind)). The scale_y_log10(labels = comma) is used to log10 of y and force the tick marks not showing scientific notation. The boxplots are sorted by median value of distance using aes(x = reorder(Kind,Distance_LY,median), y=Distance_LY, color= Kind)). And then I bolded and center the title. 
<br/>
<br/>

![picture21](https://user-images.githubusercontent.com/31257555/49928414-0a6d9400-fefb-11e8-9ea6-cbb9f18df3f3.png)
> **Figure 19.**<br/>
**Method: R**<br/>
I used geom_point () to plot this graph. The null value is removed by using ggplot(data=subset(Messier, !is.na(Kind)). The scale_y_log10(labels = comma) is used to log10 of y and force the tick marks not showing scientific notation. I used the scale_color_gradient(low="blue", high="gray") to visually differentiate the magnitude of objects, the higher the number of the fainter the object is in the sky. I set the blue standing for bright and gray standing for faint. I also set the size = Size which you can see different size of dot spread out in my graph. And then I bolded and centered the title. 
<br/>
<br/>

![picture22](https://user-images.githubusercontent.com/31257555/49928415-0a6d9400-fefb-11e8-9c1d-177d57c82757.png)
> **Figure 20.**<br/>
**Method: R**<br/>
I used geom_point () to plot this graph. The null value is removed by using ggplot(data=subset(Messier, !is.na(Kind)). The scale_y_log10(labels = comma) is used to log10 of y and force the tick marks not showing as scientific notation. I used the scale_color_gradient(low="blue", high="gray") to visually differentiate the magnitude of objects, the higher the number of the fainter the object is in the sky. I set the blue standing for bright and gray standing for faint. I also set the size = Size which you can see different size of dot spread out in my graph. What’s more, I manually set the shape using  scale_shape_manual(values=c(0,1,2,3,7,10,13)) instead of use the shape= Kind which will only give 6 types of shape which is not enough for me since I need 7 types of shape. <br/>
**Analysis:**<br/>
In this graph, it delivers four information of messier objects. The color of shape shows the level of apparent magnitude, the size of shape shows the size of objects, the type of shape shows the kind of objects, and the location of the shape shows the distance of objects. It is very easy to get information of messier object with legend. 
