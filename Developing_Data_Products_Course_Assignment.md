# Developing_Data_Products_Course_Assignment
Peter F. Symosek  
October 24, 2016  



## Famous Boston Museums


```r
date()
```

```
## [1] "Mon Oct 24 23:02:57 2016"
```

```r
library(leaflet)
```

```
## Warning: package 'leaflet' was built under R version 3.3.1
```

```r
names <- c('Museum of Fine Arts',"Isabella Stewart Gardner Museum","Museum of Science","MIT Museum","Harvard Museum of Natural History")
lat=c(42.3386,42.3382,42.3677,42.3623,42.3737135051);lon=c(-71.0941,-71.0991,-71.0709,-71.0975, -71.1093312293)
df<-data.frame(lat=lat,lon=lon,popup=names)
df %>% leaflet() %>% addTiles() %>% addMarkers(popup=df$popup)
```

```
## Assuming 'lon' and 'lat' are longitude and latitude, respectively
```

<!--html_preserve--><div id="htmlwidget-10f79ce630118d89dba9" style="width:672px;height:480px;" class="leaflet html-widget"></div>
<script type="application/json" data-for="htmlwidget-10f79ce630118d89dba9">{"x":{"calls":[{"method":"addTiles","args":["http://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png",null,null,{"minZoom":0,"maxZoom":18,"maxNativeZoom":null,"tileSize":256,"subdomains":"abc","errorTileUrl":"","tms":false,"continuousWorld":false,"noWrap":false,"zoomOffset":0,"zoomReverse":false,"opacity":1,"zIndex":null,"unloadInvisibleTiles":null,"updateWhenIdle":null,"detectRetina":false,"reuseTiles":false,"attribution":"&copy; <a href=\"http://openstreetmap.org\">OpenStreetMap\u003c/a> contributors, <a href=\"http://creativecommons.org/licenses/by-sa/2.0/\">CC-BY-SA\u003c/a>"}]},{"method":"addMarkers","args":[[42.3386,42.3382,42.3677,42.3623,42.3737135051],[-71.0941,-71.0991,-71.0709,-71.0975,-71.1093312293],null,null,null,{"clickable":true,"draggable":false,"keyboard":true,"title":"","alt":"","zIndexOffset":0,"opacity":1,"riseOnHover":false,"riseOffset":250},["Museum of Fine Arts","Isabella Stewart Gardner Museum","Museum of Science","MIT Museum","Harvard Museum of Natural History"],null,null]}],"limits":{"lat":[42.3382,42.3737135051],"lng":[-71.1093312293,-71.0709]}},"evals":[],"jsHooks":[]}</script><!--/html_preserve-->

