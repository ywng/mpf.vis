MPF Vis
=======
http://ywng.github.io/mpf.vis

Visualization of Hang Seng Bank MPF Scheme (Super Trust Plus)


It aims to provide a good visulization of time series data. 
The MPF Funds should be conveniently viewed, retrived, compared(may be). 
So, here I proposed a multi-series line plot for 
visulizing a set of MPF funds (Hang Seng Bank Super Trust Plus Scheme). Originally, the price data was fetched automatically every day. I changed to load from static file data.json so avoid web hosting need. 

It allows quick interaction with data.
The system is developed with mainly D3.js, manipulating SVG.

![alt tag](https://raw.github.com/ywng/mpf_vis/master/PrintScreen.png)

Design Characteristics:

1. Allow quick selection of the funds, and add it into the plot (click the color rect next to fund name)

2. Auto adjust of y-axis according to the selected funds

3. Allow traversal of time line quickly, quick selection of time interval (select over the yellow slider bar at the bottom)

4. Has a picker line to view the detailed price and date

5. Show price percentage changed and highlighted accordingly (red: decrease; black: increase)

6. Quick view of return of any length of time interval dated back (if no mouse move over the graph, then 1 day return / change of price will be shown, if mouse over the curve, then the return from that date (hover line) to present is shown)(E.g. in the screen shoot, the % change is the return from Apr 1, 2013 to present)

For the price data of those MPF fund, I scrapped it from Bloomberg webpage, by a servelet (see further the code on my github:https://github.com/ywng/MPF_Portal )I made, which is then trigger by an online scheduler server (cron scheduler: https://mywebcron-com.loopiasecure.com/members.php?Jobs). So, the price is 
extracted daily and updated into my database (free host: http://www.db4free.net/). After extracting the data, I also made an API url for external requesting of data.
