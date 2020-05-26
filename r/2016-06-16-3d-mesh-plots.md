---
description: How to make interactive 3D mesh plots in R.
display_as: 3d_charts
language: r
layout: base
name: 3D Mesh Plots
order: 4
output:
  html_document:
    keep_md: true
page_type: example_index
permalink: r/3d-mesh/
redirect_from: r/3d-mesh-plots/
thumbnail: thumbnail/3d-mesh.jpg
---


### Basic 3D Mesh Plot


```r
library(plotly)

x <- runif(50, 0, 1)
y <- runif(50, 0, 1)
z <- runif(50, 0, 1)

fig <- plot_ly(x = ~x, y = ~y, z = ~z, type = 'mesh3d')

fig
```

<div id="htmlwidget-27a470bae69369447379" style="width:672px;height:480px;" class="plotly html-widget"></div>
<script type="application/json" data-for="htmlwidget-27a470bae69369447379">{"x":{"visdat":{"608d4a0547cb":["function () ","plotlyVisDat"]},"cur_data":"608d4a0547cb","attrs":{"608d4a0547cb":{"x":{},"y":{},"z":{},"alpha_stroke":1,"sizes":[10,100],"spans":[1,20],"type":"mesh3d"}},"layout":{"margin":{"b":40,"l":60,"t":25,"r":10},"scene":{"xaxis":{"title":"x"},"yaxis":{"title":"y"},"zaxis":{"title":"z"}},"hovermode":"closest","showlegend":false,"legend":{"yanchor":"top","y":0.5}},"source":"A","config":{"showSendToCloud":false},"data":[{"colorbar":{"title":"z","ticklen":2,"len":0.5,"lenmode":"fraction","y":1,"yanchor":"top"},"colorscale":[["0","rgba(68,1,84,1)"],["0.0416666666666667","rgba(70,19,97,1)"],["0.0833333333333333","rgba(72,32,111,1)"],["0.125","rgba(71,45,122,1)"],["0.166666666666667","rgba(68,58,128,1)"],["0.208333333333333","rgba(64,70,135,1)"],["0.25","rgba(60,82,138,1)"],["0.291666666666667","rgba(56,93,140,1)"],["0.333333333333333","rgba(49,104,142,1)"],["0.375","rgba(46,114,142,1)"],["0.416666666666667","rgba(42,123,142,1)"],["0.458333333333333","rgba(38,133,141,1)"],["0.5","rgba(37,144,140,1)"],["0.541666666666667","rgba(33,154,138,1)"],["0.583333333333333","rgba(39,164,133,1)"],["0.625","rgba(47,174,127,1)"],["0.666666666666667","rgba(53,183,121,1)"],["0.708333333333333","rgba(79,191,110,1)"],["0.75","rgba(98,199,98,1)"],["0.791666666666667","rgba(119,207,85,1)"],["0.833333333333333","rgba(147,214,70,1)"],["0.875","rgba(172,220,52,1)"],["0.916666666666667","rgba(199,225,42,1)"],["0.958333333333333","rgba(226,228,40,1)"],["1","rgba(253,231,37,1)"]],"showscale":true,"x":[0.0811075307428837,0.93897761637345,0.452039356110618,0.13422910682857,0.633820914430544,0.627514033112675,0.0289182369597256,0.228421584703028,0.402943136170506,0.208120860857889,0.994855397613719,0.328357034595683,0.227176305372268,0.447874244302511,0.819375105667859,0.305780353257433,0.479924536542967,0.554149391362444,0.855597457615659,0.409110624110326,0.248978324700147,0.973447660217062,0.546607418218628,0.192447867244482,0.953905723057687,0.721471428172663,0.185396130895242,0.273038850864395,0.99208000022918,0.403850419213995,0.661547921830788,0.373945002676919,0.32287296350114,0.978144998429343,0.398678892524913,0.74473154800944,0.713828074978665,0.1245561176911,0.705708879977465,0.957235544919968,0.726302052848041,0.624705478083342,0.412522493163124,0.543370808241889,0.176071531372145,0.702480484033003,0.251374296145514,0.741672146134079,0.441260509658605,0.277154814219102],"y":[0.120125059736893,0.149158448446542,0.0966997570358217,0.56949798273854,0.852423338452354,0.746474325889722,0.618496972834691,0.65646750247106,0.421033999882638,0.303989277686924,0.820987307699397,0.992966032354161,0.396377900615335,0.321918129688129,0.348025804152712,0.764754853211343,0.204223827226087,0.293083738535643,0.443976380629465,0.735767727717757,0.285612974781543,0.254210932180285,0.68600197439082,0.700608305167407,0.881276015425101,0.793654788751155,0.757886294741184,0.113542284118012,0.490881344303489,0.0538067938759923,0.262545216828585,0.803923144703731,0.185067603364587,0.0308476961217821,0.225345404120162,0.399903604527935,0.335835112957284,0.863537218188867,0.445409420877695,0.818791119847447,0.120711984811351,0.739249596139416,0.698952970327809,0.338312584208325,0.452767947688699,0.0699081099592149,0.656158696627244,0.343840160174295,0.483377649448812,0.650172223802656],"z":[0.666388117941096,0.310995722422376,0.672093346249312,0.59753971779719,0.910526882391423,0.476101049687713,0.935257609235123,0.887997078010812,0.460765710799024,0.931371088372543,0.846060196636245,0.686862729955465,0.483260824345052,0.158510462846607,0.835070315282792,0.044404795859009,0.306444454705343,0.515388519736007,0.722960115177557,0.669014420593157,0.537854324094951,0.667927935253829,0.0701922602020204,0.503960790811107,0.522144541377202,0.832548945443705,0.423238535877317,0.186551009770483,0.651045373640954,0.92466623079963,0.570428828475997,0.403150398982689,0.295309601584449,0.230553685687482,0.276469562901184,0.469555805902928,0.35857574082911,0.0823521669954062,0.879327008966357,0.540615326259285,0.61791884759441,0.120584462070838,0.203846572665498,0.0666445791721344,0.645892969332635,0.821076220367104,0.765722804237157,0.0560143133625388,0.947872370947152,0.242125593591481],"type":"mesh3d","frame":null}],"highlight":{"on":"plotly_click","persistent":false,"dynamic":false,"selectize":false,"opacityDim":0.2,"selected":{"opacity":1},"debounce":0},"shinyEvents":["plotly_hover","plotly_click","plotly_selected","plotly_relayout","plotly_brushed","plotly_brushing","plotly_clickannotation","plotly_doubleclick","plotly_deselect","plotly_afterplot","plotly_sunburstclick"],"base_url":"https://plot.ly"},"evals":[],"jsHooks":[]}</script>

### Tetrahedron Mesh Plot


```r
library(plotly)

fig <- plot_ly(type = 'mesh3d',
  x = c(0, 1, 2, 0),
  y = c(0, 0, 1, 2),
  z = c(0, 2, 0, 1),
  i = c(0, 0, 0, 1),
  j = c(1, 2, 3, 2),
  k = c(2, 3, 1, 3),
  intensity = c(0, 0.33, 0.66, 1),
  color = c(0, 0.33, 0.66, 1),
  colors = colorRamp(c("red", "green", "blue"))
)

fig
```

<div id="htmlwidget-2e9af888a62f3d82201a" style="width:672px;height:480px;" class="plotly html-widget"></div>
<script type="application/json" data-for="htmlwidget-2e9af888a62f3d82201a">{"x":{"visdat":{"608d1f6d9e86":["function () ","plotlyVisDat"]},"cur_data":"608d1f6d9e86","attrs":{"608d1f6d9e86":{"x":[0,1,2,0],"y":[0,0,1,2],"z":[0,2,0,1],"i":[0,0,0,1],"j":[1,2,3,2],"k":[2,3,1,3],"intensity":[0,0.33,0.66,1],"color":[0,0.33,0.66,1],"colors":["function (x) ","roundcolor(cbind(palette[[1L]](x), palette[[2L]](x), palette[[3L]](x), ","    if (alpha) palette[[4L]](x))) * 255"],"alpha_stroke":1,"sizes":[10,100],"spans":[1,20],"type":"mesh3d"}},"layout":{"margin":{"b":40,"l":60,"t":25,"r":10},"scene":{"xaxis":{"title":[]},"yaxis":{"title":[]},"zaxis":{"title":[]}},"hovermode":"closest","showlegend":false,"legend":{"yanchor":"top","y":0.5}},"source":"A","config":{"showSendToCloud":false},"data":[{"colorbar":{"title":"","ticklen":2,"len":0.5,"lenmode":"fraction","y":1,"yanchor":"top"},"colorscale":[["0","rgba(255,0,0,1)"],["0.0416666666666667","rgba(234,21,0,1)"],["0.0833333333333333","rgba(212,42,0,1)"],["0.125","rgba(191,64,0,1)"],["0.166666666666667","rgba(170,85,0,1)"],["0.208333333333333","rgba(149,106,0,1)"],["0.25","rgba(128,128,0,1)"],["0.291666666666667","rgba(106,149,0,1)"],["0.333333333333333","rgba(85,170,0,1)"],["0.375","rgba(64,191,0,1)"],["0.416666666666667","rgba(43,212,0,1)"],["0.458333333333333","rgba(21,234,0,1)"],["0.5","rgba(0,255,0,1)"],["0.541666666666667","rgba(0,234,21,1)"],["0.583333333333333","rgba(0,213,42,1)"],["0.625","rgba(0,191,64,1)"],["0.666666666666667","rgba(0,170,85,1)"],["0.708333333333333","rgba(0,149,106,1)"],["0.75","rgba(0,128,128,1)"],["0.791666666666667","rgba(0,106,149,1)"],["0.833333333333333","rgba(0,85,170,1)"],["0.875","rgba(0,64,191,1)"],["0.916666666666667","rgba(0,43,212,1)"],["0.958333333333333","rgba(0,21,234,1)"],["1","rgba(0,0,255,1)"]],"showscale":true,"x":[0,1,2,0],"y":[0,0,1,2],"z":[0,2,0,1],"i":[0,0,0,1],"j":[1,2,3,2],"k":[2,3,1,3],"intensity":[0,0.33,0.66,1],"type":"mesh3d","marker":{"line":{"colorbar":{"title":"","ticklen":2},"cmin":0,"cmax":1,"colorscale":[["0","rgba(255,0,0,1)"],["0.0416666666666667","rgba(234,21,0,1)"],["0.0833333333333333","rgba(212,42,0,1)"],["0.125","rgba(191,64,0,1)"],["0.166666666666667","rgba(170,85,0,1)"],["0.208333333333333","rgba(149,106,0,1)"],["0.25","rgba(128,128,0,1)"],["0.291666666666667","rgba(106,149,0,1)"],["0.333333333333333","rgba(85,170,0,1)"],["0.375","rgba(64,191,0,1)"],["0.416666666666667","rgba(43,212,0,1)"],["0.458333333333333","rgba(21,234,0,1)"],["0.5","rgba(0,255,0,1)"],["0.541666666666667","rgba(0,234,21,1)"],["0.583333333333333","rgba(0,213,42,1)"],["0.625","rgba(0,191,64,1)"],["0.666666666666667","rgba(0,170,85,1)"],["0.708333333333333","rgba(0,149,106,1)"],["0.75","rgba(0,128,128,1)"],["0.791666666666667","rgba(0,106,149,1)"],["0.833333333333333","rgba(0,85,170,1)"],["0.875","rgba(0,64,191,1)"],["0.916666666666667","rgba(0,43,212,1)"],["0.958333333333333","rgba(0,21,234,1)"],["1","rgba(0,0,255,1)"]],"showscale":false,"color":[0,0.33,0.66,1]}},"frame":null}],"highlight":{"on":"plotly_click","persistent":false,"dynamic":false,"selectize":false,"opacityDim":0.2,"selected":{"opacity":1},"debounce":0},"shinyEvents":["plotly_hover","plotly_click","plotly_selected","plotly_relayout","plotly_brushed","plotly_brushing","plotly_clickannotation","plotly_doubleclick","plotly_deselect","plotly_afterplot","plotly_sunburstclick"],"base_url":"https://plot.ly"},"evals":[],"jsHooks":[]}</script>

### Cube Mesh Plot


```r
library(plotly)

fig <- plot_ly(type = 'mesh3d',
  x = c(0, 0, 1, 1, 0, 0, 1, 1),
  y = c(0, 1, 1, 0, 0, 1, 1, 0),
  z = c(0, 0, 0, 0, 1, 1, 1, 1),
  i = c(7, 0, 0, 0, 4, 4, 6, 6, 4, 0, 3, 2),
  j = c(3, 4, 1, 2, 5, 6, 5, 2, 0, 1, 6, 3),
  k = c(0, 7, 2, 3, 6, 7, 1, 1, 5, 5, 7, 6),
  intensity = seq(0, 1, length = 8),
  color = seq(0, 1, length = 8),
  colors = colorRamp(rainbow(8))
)

fig
```

<div id="htmlwidget-2116bbd6ef3d6c9ea7e7" style="width:672px;height:480px;" class="plotly html-widget"></div>
<script type="application/json" data-for="htmlwidget-2116bbd6ef3d6c9ea7e7">{"x":{"visdat":{"608dd7a2fb0":["function () ","plotlyVisDat"]},"cur_data":"608dd7a2fb0","attrs":{"608dd7a2fb0":{"x":[0,0,1,1,0,0,1,1],"y":[0,1,1,0,0,1,1,0],"z":[0,0,0,0,1,1,1,1],"i":[7,0,0,0,4,4,6,6,4,0,3,2],"j":[3,4,1,2,5,6,5,2,0,1,6,3],"k":[0,7,2,3,6,7,1,1,5,5,7,6],"intensity":[0,0.142857142857143,0.285714285714286,0.428571428571429,0.571428571428571,0.714285714285714,0.857142857142857,1],"color":[0,0.142857142857143,0.285714285714286,0.428571428571429,0.571428571428571,0.714285714285714,0.857142857142857,1],"colors":["function (x) ","roundcolor(cbind(palette[[1L]](x), palette[[2L]](x), palette[[3L]](x), ","    if (alpha) palette[[4L]](x))) * 255"],"alpha_stroke":1,"sizes":[10,100],"spans":[1,20],"type":"mesh3d"}},"layout":{"margin":{"b":40,"l":60,"t":25,"r":10},"scene":{"xaxis":{"title":[]},"yaxis":{"title":[]},"zaxis":{"title":[]}},"hovermode":"closest","showlegend":false,"legend":{"yanchor":"top","y":0.5}},"source":"A","config":{"showSendToCloud":false},"data":[{"colorbar":{"title":"","ticklen":2,"len":0.5,"lenmode":"fraction","y":1,"yanchor":"top"},"colorscale":[["0","rgba(255,0,0,1)"],["0.0416666666666667","rgba(255,56,0,1)"],["0.0833333333333333","rgba(255,111,0,1)"],["0.125","rgba(255,167,0,1)"],["0.166666666666667","rgba(234,202,0,1)"],["0.208333333333333","rgba(197,220,0,1)"],["0.25","rgba(160,239,0,1)"],["0.291666666666667","rgba(123,255,3,1)"],["0.333333333333333","rgba(85,255,21,1)"],["0.375","rgba(48,255,40,1)"],["0.416666666666667","rgba(11,255,59,1)"],["0.458333333333333","rgba(0,255,104,1)"],["0.5","rgba(0,255,160,1)"],["0.541666666666667","rgba(0,255,215,1)"],["0.583333333333333","rgba(0,239,255,1)"],["0.625","rgba(0,183,255,1)"],["0.666666666666667","rgba(0,128,255,1)"],["0.708333333333333","rgba(0,72,255,1)"],["0.75","rgba(32,48,255,1)"],["0.791666666666667","rgba(69,29,255,1)"],["0.833333333333333","rgba(107,11,255,1)"],["0.875","rgba(144,0,247,1)"],["0.916666666666667","rgba(181,0,228,1)"],["0.958333333333333","rgba(218,0,210,1)"],["1","rgba(255,0,191,1)"]],"showscale":true,"x":[0,0,1,1,0,0,1,1],"y":[0,1,1,0,0,1,1,0],"z":[0,0,0,0,1,1,1,1],"i":[7,0,0,0,4,4,6,6,4,0,3,2],"j":[3,4,1,2,5,6,5,2,0,1,6,3],"k":[0,7,2,3,6,7,1,1,5,5,7,6],"intensity":[0,0.142857142857143,0.285714285714286,0.428571428571429,0.571428571428571,0.714285714285714,0.857142857142857,1],"type":"mesh3d","marker":{"line":{"colorbar":{"title":"","ticklen":2},"cmin":0,"cmax":1,"colorscale":[["0","rgba(255,0,0,1)"],["0.0416666666666667","rgba(255,56,0,1)"],["0.0833333333333333","rgba(255,111,0,1)"],["0.125","rgba(255,167,0,1)"],["0.166666666666667","rgba(234,202,0,1)"],["0.208333333333333","rgba(197,220,0,1)"],["0.25","rgba(160,239,0,1)"],["0.291666666666667","rgba(123,255,3,1)"],["0.333333333333333","rgba(85,255,21,1)"],["0.375","rgba(48,255,40,1)"],["0.416666666666667","rgba(11,255,59,1)"],["0.458333333333333","rgba(0,255,104,1)"],["0.5","rgba(0,255,160,1)"],["0.541666666666667","rgba(0,255,215,1)"],["0.583333333333333","rgba(0,239,255,1)"],["0.625","rgba(0,183,255,1)"],["0.666666666666667","rgba(0,128,255,1)"],["0.708333333333333","rgba(0,72,255,1)"],["0.75","rgba(32,48,255,1)"],["0.791666666666667","rgba(69,29,255,1)"],["0.833333333333333","rgba(107,11,255,1)"],["0.875","rgba(144,0,247,1)"],["0.916666666666667","rgba(181,0,228,1)"],["0.958333333333333","rgba(218,0,210,1)"],["1","rgba(255,0,191,1)"]],"showscale":false,"color":[0,0.142857142857143,0.285714285714286,0.428571428571429,0.571428571428571,0.714285714285714,0.857142857142857,1]}},"frame":null}],"highlight":{"on":"plotly_click","persistent":false,"dynamic":false,"selectize":false,"opacityDim":0.2,"selected":{"opacity":1},"debounce":0},"shinyEvents":["plotly_hover","plotly_click","plotly_selected","plotly_relayout","plotly_brushed","plotly_brushing","plotly_clickannotation","plotly_doubleclick","plotly_deselect","plotly_afterplot","plotly_sunburstclick"],"base_url":"https://plot.ly"},"evals":[],"jsHooks":[]}</script>

#Reference

See [https://plotly.com/r/reference/#mesh3d](https://plotly.com/r/reference/#mesh3d) for more information and chart attribute options!

### What About Dash?

[Dash for R](https://dashr.plot.ly/) is an open-source framework for building analytical applications, with no Javascript required, and it is tightly integrated with the Plotly graphing library. 

Learn about how to install Dash for R at https://dashr.plot.ly/installation.

Everywhere in this page that you see `fig`, you can display the same figure in a Dash for R application by passing it to the `figure` argument of the [`Graph` component](https://dashr.plot.ly/dash-core-components/graph) from the built-in `dashCoreComponents` package like this:


```r
library(plotly)

fig <- plot_ly() 
# fig <- fig %>% add_trace( ... )
# fig <- fig %>% layout( ... ) 

library(dash)
library(dashCoreComponents)
library(dashHtmlComponents)

app <- Dash$new()
app$layout(
    htmlDiv(
        list(
            dccGraph(figure=fig) 
        )
     )
)

app$run_server(debug=TRUE, dev_tools_hot_reload=FALSE)
```
