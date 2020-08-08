---
title: "My First Leaflet Map"
author: "Luis Carlos Garzón"
date: "07/08/2020"
output: 
  html_document:
    keep_md: true
---

# Welcome to Bogotá Colombia

Here is my map :D

I try to cover the area of my university with the rectangle. I also point the location with a marker and added a pop-up. 




```r
library(leaflet)
uniicon<- makeIcon("https://upload.wikimedia.org/wikipedia/commons/thumb/4/47/University_of_Los_Andes_logo.svg/800px-University_of_Los_Andes_logo.svg.png" ,iconWidth =31*215/230,iconHeight = 31, iconAnchorX = 31*215/230/2, iconAnchorY = 16)

mymap<-leaflet() %>% addTiles()
unirect<-c(4.604860, -74.065885,4.600788, -74.064434)
mymap<-mymap %>% addRectangles(lng1 =unirect[2] ,lat1 = unirect[1] ,lng2 = unirect[4] ,lat2 = unirect[3])
mymap<-mymap %>% addMarkers(lng =  -74.065063, lat = 4.602859,icon = uniicon, popup = "Welcome to the best university of Colombia -QS University Ranking" )
mymap
```

<!--html_preserve--><div id="htmlwidget-6f2afbd0ffd3fbac5d13" style="width:672px;height:480px;" class="leaflet html-widget"></div>
<script type="application/json" data-for="htmlwidget-6f2afbd0ffd3fbac5d13">{"x":{"options":{"crs":{"crsClass":"L.CRS.EPSG3857","code":null,"proj4def":null,"projectedBounds":null,"options":{}}},"calls":[{"method":"addTiles","args":["//{s}.tile.openstreetmap.org/{z}/{x}/{y}.png",null,null,{"minZoom":0,"maxZoom":18,"tileSize":256,"subdomains":"abc","errorTileUrl":"","tms":false,"noWrap":false,"zoomOffset":0,"zoomReverse":false,"opacity":1,"zIndex":1,"detectRetina":false,"attribution":"&copy; <a href=\"http://openstreetmap.org\">OpenStreetMap<\/a> contributors, <a href=\"http://creativecommons.org/licenses/by-sa/2.0/\">CC-BY-SA<\/a>"}]},{"method":"addRectangles","args":[4.60486,-74.065885,4.600788,-74.064434,null,null,{"interactive":true,"className":"","stroke":true,"color":"#03F","weight":5,"opacity":0.5,"fill":true,"fillColor":"#03F","fillOpacity":0.2,"smoothFactor":1,"noClip":false},null,null,null,{"interactive":false,"permanent":false,"direction":"auto","opacity":1,"offset":[0,0],"textsize":"10px","textOnly":false,"className":"","sticky":true},null]},{"method":"addMarkers","args":[4.602859,-74.065063,{"iconUrl":{"data":"https://upload.wikimedia.org/wikipedia/commons/thumb/4/47/University_of_Los_Andes_logo.svg/800px-University_of_Los_Andes_logo.svg.png","index":0},"iconWidth":28.9782608695652,"iconHeight":31,"iconAnchorX":14.4891304347826,"iconAnchorY":16},null,null,{"interactive":true,"draggable":false,"keyboard":true,"title":"","alt":"","zIndexOffset":0,"opacity":1,"riseOnHover":false,"riseOffset":250},"Welcome to the best university of Colombia -QS University Ranking",null,null,null,null,{"interactive":false,"permanent":false,"direction":"auto","opacity":1,"offset":[0,0],"textsize":"10px","textOnly":false,"className":"","sticky":true},null]}],"limits":{"lat":[4.600788,4.60486],"lng":[-74.065885,-74.064434]}},"evals":[],"jsHooks":[]}</script><!--/html_preserve-->

