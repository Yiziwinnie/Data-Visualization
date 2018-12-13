# Data-Visualization
R &amp; Tableau
![picture1](https://user-images.githubusercontent.com/31257555/49926419-7b5e7d00-fef6-11e8-8ef1-1071c5de0a98.png)
> **Figure 1.**
I selected date as Exact date in Tableau. The title is bold displaying in center of figure. The label of x axis is reset with only Year 1998 and y axis is added dollar sign. The color of line is red instead of using default color and the color of tick marker is reset in orange. 
<br/>
<br/>

![picture2](https://user-images.githubusercontent.com/31257555/49926425-7f8a9a80-fef6-11e8-91ac-5eef2eb391bc.png)
> **Figure 2.**
I selected date as Exact date in Tableau. The title is bold displaying in center of figure. The label of x axis is reset with only Year 1998. The color of bar is blue which is matched with the real visualization of stock market. I also reset the size of bar that we can see daily record avoid too much overlapping issue. 
<br/>
<br/>

![picture3](https://user-images.githubusercontent.com/31257555/49926426-7f8a9a80-fef6-11e8-9c40-84b3b9f64063.png)
> **Figure 3.**
The title is bold displaying in center of figure. The color of bar is green instead of using default color. I tried to rest the scale the tick. However, there are some records locating in range of 360M to 380M. The width of bar is also changed which is a little bit narrower than the default width. The figure showing as above is the best after many times of adjustments. 
Because there is one outlier here, I just indented keep it to show all information. 


![picture4](https://user-images.githubusercontent.com/31257555/49926427-7f8a9a80-fef6-11e8-896b-0854aace8782.png)
> **Figure 4.**
The title is bold displaying in center of figure. The y axis is added dollar sign. A new column named Range is added into dataset by setting Calculated Field with ([High]-[low]). The color of point varies in four colors as you see in the legend. Some extra hidden information can get from this setting. For example, the range is gradually larger with the trading day. I also reset the size of point instead of using default value. Because there is one outlier here, I just indented keep it to show all information. 
<br/>
<br/>

![picture5](https://user-images.githubusercontent.com/31257555/49926428-80233100-fef6-11e8-94dd-23b2154fcda1.png)
> **Figure 5.**
The title is bold displaying in center of figure. The label of x axis is reset with only Error. In order to explain what the error is, I added a brace with explanation. The color of bar is pink instead of using default color. A new column named Error is added into dataset by setting Calculated Field with ([Response]-[TrueValue]).

<br/>
<br/>

![picture6](https://user-images.githubusercontent.com/31257555/49926431-80233100-fef6-11e8-9778-33db11dd67d0.png)
> **Figure 6.**
The title is bold displaying in center of figure. The label of x axis is indented hidden. The tick marker is reset with shorten words. I selected reservation as color to display my figure. That’s why you can see different colors of bars. What’s more, the median is used instead of using sum and the x- value is sorted. 

<br/>
<br/>

![picture7](https://user-images.githubusercontent.com/31257555/49926432-80bbc780-fef6-11e8-9f5c-3564245acc17.png)
> **Figure 7.**
The title is bold displaying in center of figure. The label of x axis is indented hidden. The tick marker is reset with shorten words. The color of bar is green instead of using default color. What’s more, the standard deviation is used instead of using sum. 
<br/>
<br/>


![picture8](https://user-images.githubusercontent.com/31257555/49926434-81545e00-fef6-11e8-87b3-e0f8cf9535c5.png)
> **Figure 8.** A new column named AbsoluteError is added into dataset by setting Calculated Field with (abs[Error]). The title is bold displaying in center of figure. The label of x axis is indented hidden. The tick marker is reset with shorten words. I selected reservation as color to display my figure, that’s why you can see different colors of bars. What’s more, the median is used instead of using sum and the x- value is sorted. <br/>
**Analysis:**<br/>
From Figure 6, The distribution of Error caculated by Response subtract TrueValue display normal distribution. Almost people will make a little bit error and fewer of them have huge visual error. From Figure 7, responses are inclined to largely underestimate the value compared with that of original color, while they largely overestimate the value compared with that of original one when perceiving volume and slope. From Figure 8, It is easier for response to compare the vertical aligned distance while much harder to compare the vertical unaligned distance. The hardest task is perceiving the slope for response. From Figure 8, response will larger mistake when perceiving color and slope compared with other shapes. 

<br/>
<br/>

![picture9](https://user-images.githubusercontent.com/31257555/49926446-874a3f00-fef6-11e8-95ff-ac0bbefb6a2a.png)
> **Figure 9.**
I used the R to complete this question. The sex is differentiated by two colors and two shapes because I think is easy for people to recognize and avoid the overlap issue as much as possible. The size and content labels of x-axis and y-axis are reset to keep their size smaller than title and more clarify with units. I tried using the shadow under separate trend lines, but the effect of it looks not good as you can see in Figure 3 b1. I made decision on only adding two separate trends and their color correspond to their classes (F, M).
<br/>
<br/>

![picture10](https://user-images.githubusercontent.com/31257555/49926449-874a3f00-fef6-11e8-882f-095968011ebb.png)
> **Figure 10.**
I clicked Show Me on the toolbar, then selected the treemap chart type. The title is bold displaying in center of figure. In order to show all information including Make, Mode, and price in my figure, I selected three of them as label and adjusted their size. The Make is also selected as color that we can see the same Make is in same color. What’s more, the mean is used instead of using sum.  
<br/>
<br/>


![picture11](https://user-images.githubusercontent.com/31257555/49926452-874a3f00-fef6-11e8-8a78-66e4832bc74f.png)
> **Figure 11.**
I clicked Show Me on the toolbar, then selected the packed bubble chart type. The title is bold displaying in center of figure. In order to show all information including Make, Mode, and price in my figure, I selected three of them as my label and adjust their size. The Make is also selected as color that we can see the same Make is in same color. What’s more, the mean is used instead of using sum. 
<br/>
<br/>


![picture12](https://user-images.githubusercontent.com/31257555/49926453-87e2d580-fef6-11e8-8eab-62aeee9edcde.png)
> **Figure 12.**
The title is bold displaying in center of figure. The label of x axis is indented hidden. The tick marker is reset with shorten words. I selected location as my column and year as color. That’s why you can see the different color corresponds to different year. 
<br/>
<br/>

![picture13](https://user-images.githubusercontent.com/31257555/49926454-87e2d580-fef6-11e8-8825-9488640eaa0d.png)
> **Figure 13.**
The title is bold displaying in center of figure. The label of x axis is indented hidden. I selected year as my column and location as color. That’s why you can see the different color corresponds to different reservation. 
<br/>
<br/>

![picture14](https://user-images.githubusercontent.com/31257555/49926455-887b6c00-fef6-11e8-9bbb-3caaa0b8b112.png)
> **Figure 14.**
I clicked Show Me in the toolbar, then selected the box-and-whisker plot chart type. The title is bold displaying in center of figure. The label of x axis is indented hidden. The tick marker is reset with shorten words. I selected location as my column and year as color. That’s why you can see the different color corresponds to different reservation. 
