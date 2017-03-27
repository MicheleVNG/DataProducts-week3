# My Presentation
Michele Vangelista  
27 march 2017  



## My Plot

The following slide presents a plot that makes use of the `Quandl` library
for retrieving US GDP data, and creates a simple plot with that.


```r
library(Quandl)
library(plotly)

df <- Quandl("FRED/GDP")
plot_ly(df, x = ~DATE, y = ~VALUE, mode = "scatter")
```

## United States GDP over time

There we go!

<!--html_preserve--><div id="htmlwidget-2f51881541d9ef50e6f7" style="width:720px;height:432px;" class="plotly html-widget"></div>
<script type="application/json" data-for="htmlwidget-2f51881541d9ef50e6f7">{"x":{"layout":{"margin":{"b":40,"l":60,"t":25,"r":10},"xaxis":{"domain":[0,1],"title":"DATE"},"yaxis":{"domain":[0,1],"title":"VALUE"}},"source":"A","config":{"modeBarButtonsToAdd":[{"name":"Collaborate","icon":{"width":1000,"ascent":500,"descent":-50,"path":"M487 375c7-10 9-23 5-36l-79-259c-3-12-11-23-22-31-11-8-22-12-35-12l-263 0c-15 0-29 5-43 15-13 10-23 23-28 37-5 13-5 25-1 37 0 0 0 3 1 7 1 5 1 8 1 11 0 2 0 4-1 6 0 3-1 5-1 6 1 2 2 4 3 6 1 2 2 4 4 6 2 3 4 5 5 7 5 7 9 16 13 26 4 10 7 19 9 26 0 2 0 5 0 9-1 4-1 6 0 8 0 2 2 5 4 8 3 3 5 5 5 7 4 6 8 15 12 26 4 11 7 19 7 26 1 1 0 4 0 9-1 4-1 7 0 8 1 2 3 5 6 8 4 4 6 6 6 7 4 5 8 13 13 24 4 11 7 20 7 28 1 1 0 4 0 7-1 3-1 6-1 7 0 2 1 4 3 6 1 1 3 4 5 6 2 3 3 5 5 6 1 2 3 5 4 9 2 3 3 7 5 10 1 3 2 6 4 10 2 4 4 7 6 9 2 3 4 5 7 7 3 2 7 3 11 3 3 0 8 0 13-1l0-1c7 2 12 2 14 2l218 0c14 0 25-5 32-16 8-10 10-23 6-37l-79-259c-7-22-13-37-20-43-7-7-19-10-37-10l-248 0c-5 0-9-2-11-5-2-3-2-7 0-12 4-13 18-20 41-20l264 0c5 0 10 2 16 5 5 3 8 6 10 11l85 282c2 5 2 10 2 17 7-3 13-7 17-13z m-304 0c-1-3-1-5 0-7 1-1 3-2 6-2l174 0c2 0 4 1 7 2 2 2 4 4 5 7l6 18c0 3 0 5-1 7-1 1-3 2-6 2l-173 0c-3 0-5-1-8-2-2-2-4-4-4-7z m-24-73c-1-3-1-5 0-7 2-2 3-2 6-2l174 0c2 0 5 0 7 2 3 2 4 4 5 7l6 18c1 2 0 5-1 6-1 2-3 3-5 3l-174 0c-3 0-5-1-7-3-3-1-4-4-5-6z"},"click":"function(gd) { \n        // is this being viewed in RStudio?\n        if (location.search == '?viewer_pane=1') {\n          alert('To learn about plotly for collaboration, visit:\\n https://cpsievert.github.io/plotly_book/plot-ly-for-collaboration.html');\n        } else {\n          window.open('https://cpsievert.github.io/plotly_book/plot-ly-for-collaboration.html', '_blank');\n        }\n      }"}],"modeBarButtonsToRemove":["sendDataToCloud"]},"data":[{"x":["2016-10-01","2016-07-01","2016-04-01","2016-01-01","2015-10-01","2015-07-01","2015-04-01","2015-01-01","2014-10-01","2014-07-01","2014-04-01","2014-01-01","2013-10-01","2013-07-01","2013-04-01","2013-01-01","2012-10-01","2012-07-01","2012-04-01","2012-01-01","2011-10-01","2011-07-01","2011-04-01","2011-01-01","2010-10-01","2010-07-01","2010-04-01","2010-01-01","2009-10-01","2009-07-01","2009-04-01","2009-01-01","2008-10-01","2008-07-01","2008-04-01","2008-01-01","2007-10-01","2007-07-01","2007-04-01","2007-01-01","2006-10-01","2006-07-01","2006-04-01","2006-01-01","2005-10-01","2005-07-01","2005-04-01","2005-01-01","2004-10-01","2004-07-01","2004-04-01","2004-01-01","2003-10-01","2003-07-01","2003-04-01","2003-01-01","2002-10-01","2002-07-01","2002-04-01","2002-01-01","2001-10-01","2001-07-01","2001-04-01","2001-01-01","2000-10-01","2000-07-01","2000-04-01","2000-01-01","1999-10-01","1999-07-01","1999-04-01","1999-01-01","1998-10-01","1998-07-01","1998-04-01","1998-01-01","1997-10-01","1997-07-01","1997-04-01","1997-01-01","1996-10-01","1996-07-01","1996-04-01","1996-01-01","1995-10-01","1995-07-01","1995-04-01","1995-01-01","1994-10-01","1994-07-01","1994-04-01","1994-01-01","1993-10-01","1993-07-01","1993-04-01","1993-01-01","1992-10-01","1992-07-01","1992-04-01","1992-01-01","1991-10-01","1991-07-01","1991-04-01","1991-01-01","1990-10-01","1990-07-01","1990-04-01","1990-01-01","1989-10-01","1989-07-01","1989-04-01","1989-01-01","1988-10-01","1988-07-01","1988-04-01","1988-01-01","1987-10-01","1987-07-01","1987-04-01","1987-01-01","1986-10-01","1986-07-01","1986-04-01","1986-01-01","1985-10-01","1985-07-01","1985-04-01","1985-01-01","1984-10-01","1984-07-01","1984-04-01","1984-01-01","1983-10-01","1983-07-01","1983-04-01","1983-01-01","1982-10-01","1982-07-01","1982-04-01","1982-01-01","1981-10-01","1981-07-01","1981-04-01","1981-01-01","1980-10-01","1980-07-01","1980-04-01","1980-01-01","1979-10-01","1979-07-01","1979-04-01","1979-01-01","1978-10-01","1978-07-01","1978-04-01","1978-01-01","1977-10-01","1977-07-01","1977-04-01","1977-01-01","1976-10-01","1976-07-01","1976-04-01","1976-01-01","1975-10-01","1975-07-01","1975-04-01","1975-01-01","1974-10-01","1974-07-01","1974-04-01","1974-01-01","1973-10-01","1973-07-01","1973-04-01","1973-01-01","1972-10-01","1972-07-01","1972-04-01","1972-01-01","1971-10-01","1971-07-01","1971-04-01","1971-01-01","1970-10-01","1970-07-01","1970-04-01","1970-01-01","1969-10-01","1969-07-01","1969-04-01","1969-01-01","1968-10-01","1968-07-01","1968-04-01","1968-01-01","1967-10-01","1967-07-01","1967-04-01","1967-01-01","1966-10-01","1966-07-01","1966-04-01","1966-01-01","1965-10-01","1965-07-01","1965-04-01","1965-01-01","1964-10-01","1964-07-01","1964-04-01","1964-01-01","1963-10-01","1963-07-01","1963-04-01","1963-01-01","1962-10-01","1962-07-01","1962-04-01","1962-01-01","1961-10-01","1961-07-01","1961-04-01","1961-01-01","1960-10-01","1960-07-01","1960-04-01","1960-01-01","1959-10-01","1959-07-01","1959-04-01","1959-01-01","1958-10-01","1958-07-01","1958-04-01","1958-01-01","1957-10-01","1957-07-01","1957-04-01","1957-01-01","1956-10-01","1956-07-01","1956-04-01","1956-01-01","1955-10-01","1955-07-01","1955-04-01","1955-01-01","1954-10-01","1954-07-01","1954-04-01","1954-01-01","1953-10-01","1953-07-01","1953-04-01","1953-01-01","1952-10-01","1952-07-01","1952-04-01","1952-01-01","1951-10-01","1951-07-01","1951-04-01","1951-01-01","1950-10-01","1950-07-01","1950-04-01","1950-01-01","1949-10-01","1949-07-01","1949-04-01","1949-01-01","1948-10-01","1948-07-01","1948-04-01","1948-01-01","1947-10-01","1947-07-01","1947-04-01","1947-01-01"],"y":[18855.5,18675.3,18450.1,18281.6,18222.8,18141.9,17998.3,17783.6,17692.2,17569.4,17285.6,17025.2,16999.9,16749.3,16541.4,16475.4,16297.3,16227.9,16121.9,15973.9,15785.3,15587.1,15460.9,15238.4,15230.2,15057.7,14888.6,14681.1,14566.5,14384.1,14340.4,14383.9,14549.9,14843,14813,14668.4,14685.3,14569.7,14422.3,14233.2,14066.4,13908.5,13799.8,13648.9,13381.6,13205.4,12974.1,12813.7,12562.2,12367.7,12181.4,11988.4,11816.8,11625.1,11370.7,11230.1,11103.8,11037.1,10934.8,10834.4,10701.3,10639.5,10638.4,10508.1,10472.3,10357.4,10278.3,10031,9926.1,9712.3,9557,9447.1,9325.7,9146.5,8994.7,8889.7,8788.3,8691.8,8551.9,8402.1,8287.1,8159,8061.5,7893.1,7799.5,7706.5,7604.9,7545.3,7476.7,7352.3,7269.8,7136.3,7032.8,6904.2,6829.6,6748.2,6697.6,6586.5,6492.3,6380.8,6279.3,6218.4,6143.6,6054.9,6023.3,6029.5,5974.7,5890.8,5763.4,5711.6,5628.4,5527.4,5412.7,5299.5,5207.7,5090.6,5022.7,4900.5,4821.5,4736.2,4669.4,4619.6,4555.2,4516.3,4453.1,4394.6,4302.3,4237,4147.6,4087.4,4015,3912.8,3796.1,3692.3,3583.8,3480.3,3407.8,3367.1,3331.3,3273.8,3283.5,3261.2,3167.3,3131.8,2993.5,2860,2799.9,2796.5,2730.7,2670.4,2595.9,2531.6,2482.2,2398.9,2336.6,2208.7,2168.7,2122.4,2060.2,1992.5,1938.4,1890.5,1856.9,1824.5,1765.9,1713.8,1656.4,1619.6,1603,1563.4,1534.2,1494.7,1479.1,1436.8,1417.6,1380.7,1332,1293.8,1270.1,1233.8,1193.6,1180.3,1159.4,1137.8,1091.5,1088.5,1070.1,1053.5,1040.7,1032,1011.4,995.4,970.1,952.3,936.3,911.1,883.2,866.6,851.1,846,834.9,820.8,807.2,797.3,773.1,750.2,732.4,719.2,698.4,692.8,680.8,671.1,654.8,645,631.8,622.7,613.1,609.6,602.6,595.2,581.6,568.2,557.4,545.9,541.1,546,542.7,543.3,529.3,525.2,524.2,511.1,500.4,486.7,472.8,468.4,475.7,480.3,472.8,470.6,461.3,452,446.8,440.5,437.8,430.9,422.2,413.8,400.3,391.6,386.7,385.9,386.5,391.7,392.3,388.5,381.2,368.1,361.4,360.2,356.6,351.8,344.5,336.4,320.3,308.5,290.7,281.2,271,273.3,271.7,275.4,280.7,279.5,272.9,266.2,260.3,250.1,246.3,243.1],"mode":"scatter","type":"scatter","xaxis":"x","yaxis":"y"}],"base_url":"https://plot.ly"},"evals":["config.modeBarButtonsToAdd.0.click"],"jsHooks":[]}</script><!--/html_preserve-->


# Thanks