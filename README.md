MPF Vis
=======

Visualization of Hang Seng Bank MPF Scheme (Super Trust Plus)


It aims to provide a good visulization of time series data. 
The MPF Funds should be conveniently viewed, retrived, compared(may be). 
So, here I proposed a multi-series line plot for 
visulizing a set of MPF funds (Hang Seng Bank Super Trust Plus Scheme).

It allows quick interaction with data.
The system is developed with mainly D3.js, manipulating SVG.
Have a look at it: http://mpf.vis.ywng.cloudbees.net/

Design Characteristics:
1. Allow quick selection of the funds, and add it into the plot (click the color rect next to fund name)
2. Auto adjust of y-axis according to the selected funds
3. Allow traversal of time line quickly, quick selection of time interval
4. Has a picker line to view the detailed price and date
5. Show price percentage changed and highlighted accordingly (red: decrease; black: increase)

For the price data of those MPF fund, I scrapped it from Bloomberg webpage, by a servelet (see further the code on my github:https://github.com/ywng/MPF_Portal )I made, which is then trigger by an online scheduler server (cron scheduler: https://mywebcron-com.loopiasecure.com/members.php?Jobs). So, the price is 
extracted daily and updated into my database (free host: http://www.db4free.net/). After extracting the data, I also made an API url for external requesting of data.
