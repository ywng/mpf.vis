mpf_vis
=======

Visualization of Hang Seng Bank MPF Scheme (Super Trust Plus)


It aims to provide a good visulization of time series data. 
The MPF Funds should be conveniently viewed, retrived, compared(may be). So, here I proposed a multi-series line plot for 
visulizing a set of MPF funds (Hang Seng Bank Super Trust Plus Scheme).

It allows quick interaction with data.
The system is developed with mainly D3.js, manipulating SVG.
Have a look at it: http://mpf.vis.ywng.cloudbees.net/

For the price data of those MPF fund, I scrapped it from Bloomberg webpage, by a servelet (see further the code on my github:
)I made, which is then trigger by an online scheduler server (cron scheduler: https://mywebcron-com.loopiasecure.com/members.php?Jobs). So, the price is 
extracted daily and updated into my database (free host: http://www.db4free.net/).
