# Build-a-Stock-Watchlist-with-Live-Data-in-Google-Sheets

What you can do in this sheet -

➟ How to structure your Google Sheet for optimal stock data tracking.

➟ Techniques for fetching real-time stock information using formulas.

➟ Tips for integrating additional metrics like 52 High, 52 Low, Market Cap, PE, and more. 

➟ Ideas for visualizing trends with a 250-day chart.

# Product Description

Maintain stock watchlist in google sheet. In this you can create your own custom stock watchlist.

In this we can track -

1.Stock Price

  Open Price =GOOGLEFINANCE(A2,"priceopen")
  
2.Stock Day Opening Price, Day High and Day Low Price

  High =GOOGLEFINANCE(A2,"High")
  
  Low =GOOGLEFINANCE(A2,"low")
  
3.Previous Day Close Price and Last Trading Price

  Prev Close =GOOGLEFINANCE(A2,"Closeyest")
  
  LTP =GOOGLEFINANCE(A2,"price")
  
4.Day Change (In Amount Or %Age)

  Change =GOOGLEFINANCE(A2,"change")
  
  Change % =GOOGLEFINANCE(A2,"changepct")/100
  
5.Day Volume, 

  Volume =GOOGLEFINANCE(A2,"volume")
  
6.Stock Market Cap, Stock PE

  MarketCap =GOOGLEFINANCE(A2,"marketcap")
  
  PE =GOOGLEFINANCE(A2,"pe")
  
7.52 Day High Or 52 Day Low 

  52 High =GOOGLEFINANCE(A2,"high52")
  
  52 Low  =GOOGLEFINANCE(A2,"low52")
  
8.5 Day Or 30-Day Change (In %Age) (We Can Change the Number of Day)

  5 Day % =F2/ INDEX(GOOGLEFINANCE(A2,"price",WORKDAY(TODAY(),-$N$1)),2,2)-1
  
  30 Day % =F2/ INDEX(GOOGLEFINANCE(A2,"price",WORKDAY(TODAY(),-$O$1)),2,2)-1
  
9.Last 250 Day Chart (We Can Change the Number of Day)

  100 Day Chart =SPARKLINE(INDEX(GOOGLEFINANCE(A2,"PRICE",WORKDAY(TODAY(),-$P$1),TODAY()),,2),{"charttype","column";"color","green"})












