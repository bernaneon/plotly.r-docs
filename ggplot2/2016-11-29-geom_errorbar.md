---
name: geom_errorbar
permalink: ggplot2/geom_errorbar/
description: Examples of geom_errobar in R and ggplot2
layout: base
thumbnail: thumbnail/error-bar.jpg
language: ggplot2
page_type: example_index
display_as: statistics
order: 2
output:
  html_document:
    keep_md: true
---


### Basic Error Bar


```r
library(plotly)

df <- data.frame(x = 1:10,
                 y = 1:10,
                 ymin = (1:10) - runif(10),
                 ymax = (1:10) + runif(10),
                 xmin = (1:10) - runif(10),
                 xmax = (1:10) + runif(10))

p <- ggplot(data = df,aes(x = x,y = y)) + 
    geom_point() + 
    geom_errorbar(aes(ymin = ymin,ymax = ymax)) + 
    geom_errorbarh(aes(xmin = xmin,xmax = xmax))

fig <- ggplotly(p)

fig
```

<div id="htmlwidget-f04c6519a944dbaff343" style="width:672px;height:480px;" class="plotly html-widget"></div>
<script type="application/json" data-for="htmlwidget-f04c6519a944dbaff343">{"x":{"data":[{"x":[1,2,3,4,5,6,7,8,9,10],"y":[1,2,3,4,5,6,7,8,9,10],"text":["x:  1<br />y:  1","x:  2<br />y:  2","x:  3<br />y:  3","x:  4<br />y:  4","x:  5<br />y:  5","x:  6<br />y:  6","x:  7<br />y:  7","x:  8<br />y:  8","x:  9<br />y:  9","x: 10<br />y: 10"],"type":"scatter","mode":"markers","marker":{"autocolorscale":false,"color":"rgba(0,0,0,1)","opacity":1,"size":5.66929133858268,"symbol":"circle","line":{"width":1.88976377952756,"color":"rgba(0,0,0,1)"}},"hoveron":"points","showlegend":false,"xaxis":"x","yaxis":"y","hoverinfo":"text","frame":null},{"x":[1,2,3,4,5,6,7,8,9,10],"y":[1,2,3,4,5,6,7,8,9,10],"text":["ymin: 0.810797<br />ymax:  1.004294<br />x:  1<br />y:  1","ymin: 1.511347<br />ymax:  2.400186<br />x:  2<br />y:  2","ymin: 2.701702<br />ymax:  3.569583<br />x:  3<br />y:  3","ymin: 3.705461<br />ymax:  4.050694<br />x:  4<br />y:  4","ymin: 4.504525<br />ymax:  5.881798<br />x:  5<br />y:  5","ymin: 5.142790<br />ymax:  6.965601<br />x:  6<br />y:  6","ymin: 6.068314<br />ymax:  7.434390<br />x:  7<br />y:  7","ymin: 7.433818<br />ymax:  8.734025<br />x:  8<br />y:  8","ymin: 8.275950<br />ymax:  9.675270<br />x:  9<br />y:  9","ymin: 9.988894<br />ymax: 10.980191<br />x: 10<br />y: 10"],"type":"scatter","mode":"lines","opacity":1,"line":{"color":"transparent"},"error_y":{"array":[0.0042942319996655,0.400186032289639,0.569583325879648,0.0506944407243282,0.881798092043027,0.96560057811439,0.434390431502834,0.734024849254638,0.675269723171368,0.980191352544352],"arrayminus":[0.189202992711216,0.488652616739273,0.298297534696758,0.294539155671373,0.495474903378636,0.857209923444316,0.931685874937102,0.566181684145704,0.724049795651808,0.0111064238008112],"type":"data","width":18.4366031490586,"symmetric":false,"color":"rgba(0,0,0,1)"},"showlegend":false,"xaxis":"x","yaxis":"y","hoverinfo":"text","frame":null},{"x":[1,2,3,4,5,6,7,8,9,10],"y":[1,2,3,4,5,6,7,8,9,10],"text":["xmin: 0.5093007<br />xmax:  1.864476<br />x:  1<br />y:  1","xmin: 1.1723474<br />xmax:  2.427868<br />x:  2<br />y:  2","xmin: 2.4879512<br />xmax:  3.397321<br />x:  3<br />y:  3","xmin: 3.0455101<br />xmax:  4.896529<br />x:  4<br />y:  4","xmin: 4.0803959<br />xmax:  5.689756<br />x:  5<br />y:  5","xmin: 5.2705511<br />xmax:  6.997863<br />x:  6<br />y:  6","xmin: 6.0929346<br />xmax:  7.872807<br />x:  7<br />y:  7","xmin: 7.8700569<br />xmax:  8.171810<br />x:  8<br />y:  8","xmin: 8.9960099<br />xmax:  9.351063<br />x:  9<br />y:  9","xmin: 9.6277115<br />xmax: 10.254427<br />x: 10<br />y: 10"],"type":"scatter","mode":"lines","opacity":1,"line":{"color":"transparent"},"error_x":{"array":[0.8644759808667,0.42786756483838,0.397320857970044,0.896529348101467,0.689756342442706,0.997862879186869,0.872807105770335,0.171809730352834,0.351062879431993,0.254427240230143],"arrayminus":[0.490699259564281,0.827652561012655,0.512048794189468,0.954489851603284,0.919604076072574,0.729448918718845,0.907065360806882,0.129943109117448,0.00399005203507841,0.372288511367515],"type":"data","width":12.5509769173273,"symmetric":false,"color":"rgba(0,0,0,1)"},"showlegend":false,"xaxis":"x","yaxis":"y","hoverinfo":"text","frame":null}],"layout":{"margin":{"t":26.2283105022831,"r":7.30593607305936,"b":40.1826484018265,"l":31.4155251141553},"plot_bgcolor":"rgba(235,235,235,1)","paper_bgcolor":"rgba(255,255,255,1)","font":{"color":"rgba(0,0,0,1)","family":"","size":14.6118721461187},"xaxis":{"domain":[0,1],"automargin":true,"type":"linear","autorange":false,"range":[0.0122657774575055,10.9470349629782],"tickmode":"array","ticktext":["2.5","5.0","7.5","10.0"],"tickvals":[2.5,5,7.5,10],"categoryorder":"array","categoryarray":["2.5","5.0","7.5","10.0"],"nticks":null,"ticks":"outside","tickcolor":"rgba(51,51,51,1)","ticklen":3.65296803652968,"tickwidth":0.66417600664176,"showticklabels":true,"tickfont":{"color":"rgba(77,77,77,1)","family":"","size":11.689497716895},"tickangle":-0,"showline":false,"linecolor":null,"linewidth":0,"showgrid":true,"gridcolor":"rgba(255,255,255,1)","gridwidth":0.66417600664176,"zeroline":false,"anchor":"y","title":{"text":"x","font":{"color":"rgba(0,0,0,1)","family":"","size":14.6118721461187}},"hoverformat":".2f"},"yaxis":{"domain":[0,1],"automargin":true,"type":"linear","autorange":false,"range":[0.0284904323727825,11.5017009201716],"tickmode":"array","ticktext":["3","6","9"],"tickvals":[3,6,9],"categoryorder":"array","categoryarray":["3","6","9"],"nticks":null,"ticks":"outside","tickcolor":"rgba(51,51,51,1)","ticklen":3.65296803652968,"tickwidth":0.66417600664176,"showticklabels":true,"tickfont":{"color":"rgba(77,77,77,1)","family":"","size":11.689497716895},"tickangle":-0,"showline":false,"linecolor":null,"linewidth":0,"showgrid":true,"gridcolor":"rgba(255,255,255,1)","gridwidth":0.66417600664176,"zeroline":false,"anchor":"x","title":{"text":"y","font":{"color":"rgba(0,0,0,1)","family":"","size":14.6118721461187}},"hoverformat":".2f"},"shapes":[{"type":"rect","fillcolor":null,"line":{"color":null,"width":0,"linetype":[]},"yref":"paper","xref":"paper","x0":0,"x1":1,"y0":0,"y1":1}],"showlegend":false,"legend":{"bgcolor":"rgba(255,255,255,1)","bordercolor":"transparent","borderwidth":1.88976377952756,"font":{"color":"rgba(0,0,0,1)","family":"","size":11.689497716895}},"hovermode":"closest","barmode":"relative"},"config":{"doubleClick":"reset","showSendToCloud":false},"source":"A","attrs":{"76615962d104":{"x":{},"y":{},"type":"scatter"},"76611964a86b":{"ymin":{},"ymax":{},"x":{},"y":{}},"766178d6c72a":{"xmin":{},"xmax":{},"x":{},"y":{}}},"cur_data":"76615962d104","visdat":{"76615962d104":["function (y) ","x"],"76611964a86b":["function (y) ","x"],"766178d6c72a":["function (y) ","x"]},"highlight":{"on":"plotly_click","persistent":false,"dynamic":false,"selectize":false,"opacityDim":0.2,"selected":{"opacity":1},"debounce":0},"shinyEvents":["plotly_hover","plotly_click","plotly_selected","plotly_relayout","plotly_brushed","plotly_brushing","plotly_clickannotation","plotly_doubleclick","plotly_deselect","plotly_afterplot","plotly_sunburstclick"],"base_url":"https://plot.ly"},"evals":[],"jsHooks":[]}</script>

### Margin Error Bar


```r
library(plotly)

population <- data.frame(Year=seq(1790, 1970, length.out=length(uspop)), 
                         Population=uspop, 
                         Error=rnorm(length(uspop), 5))

library(ggplot2)
p <- ggplot(population, aes(x=Year, y=Population, 
                       ymin=Population-Error, ymax=Population+Error))+
  geom_line()+
  geom_point(pch=2)+
  geom_errorbar(width=0.9)

fig <- ggplotly(p)

fig
```

<div id="htmlwidget-a21902059ffc0b307361" style="width:672px;height:480px;" class="plotly html-widget"></div>
<script type="application/json" data-for="htmlwidget-a21902059ffc0b307361">{"x":{"data":[{"x":[1790,1800,1810,1820,1830,1840,1850,1860,1870,1880,1890,1900,1910,1920,1930,1940,1950,1960,1970],"y":[3.93,5.31,7.24,9.64,12.9,17.1,23.2,31.4,39.8,50.2,62.9,76,92,105.7,122.8,131.7,151.3,179.3,203.2],"text":["Year: 1790<br />Population:   3.93<br />Population - Error:  -0.5471562<br />Population + Error:   8.407156","Year: 1800<br />Population:   5.31<br />Population - Error:   0.4337073<br />Population + Error:  10.186293","Year: 1810<br />Population:   7.24<br />Population - Error:   1.6991115<br />Population + Error:  12.780888","Year: 1820<br />Population:   9.64<br />Population - Error:   4.8887273<br />Population + Error:  14.391273","Year: 1830<br />Population:  12.90<br />Population - Error:   8.6903543<br />Population + Error:  17.109646","Year: 1840<br />Population:  17.10<br />Population - Error:  11.9065583<br />Population + Error:  22.293442","Year: 1850<br />Population:  23.20<br />Population - Error:  20.0621162<br />Population + Error:  26.337884","Year: 1860<br />Population:  31.40<br />Population - Error:  25.4890187<br />Population + Error:  37.310981","Year: 1870<br />Population:  39.80<br />Population - Error:  33.4809752<br />Population + Error:  46.119025","Year: 1880<br />Population:  50.20<br />Population - Error:  44.3907375<br />Population + Error:  56.009262","Year: 1890<br />Population:  62.90<br />Population - Error:  57.8318408<br />Population + Error:  67.968159","Year: 1900<br />Population:  76.00<br />Population - Error:  71.2953867<br />Population + Error:  80.704613","Year: 1910<br />Population:  92.00<br />Population - Error:  87.8781397<br />Population + Error:  96.121860","Year: 1920<br />Population: 105.70<br />Population - Error: 100.1731236<br />Population + Error: 111.226876","Year: 1930<br />Population: 122.80<br />Population - Error: 118.2524078<br />Population + Error: 127.347592","Year: 1940<br />Population: 131.70<br />Population - Error: 124.7001616<br />Population + Error: 138.699838","Year: 1950<br />Population: 151.30<br />Population - Error: 145.9902854<br />Population + Error: 156.609715","Year: 1960<br />Population: 179.30<br />Population - Error: 175.8366473<br />Population + Error: 182.763353","Year: 1970<br />Population: 203.20<br />Population - Error: 197.9800000<br />Population + Error: 208.420000"],"type":"scatter","mode":"lines+markers","line":{"width":1.88976377952756,"color":"transparent","dash":"solid"},"hoveron":"points","showlegend":false,"xaxis":"x","yaxis":"y","hoverinfo":"text","marker":{"autocolorscale":false,"color":"rgba(0,0,0,1)","opacity":1,"size":5.66929133858268,"symbol":"triangle-up-open","line":{"width":1.88976377952756,"color":"rgba(0,0,0,1)"}},"opacity":1,"error_y":{"array":[4.47715615918023,4.87629270306697,5.54088845026394,4.75127266783613,4.20964567999614,5.19344169579826,3.13788381396218,5.9109813017208,6.31902476858055,5.80926247644601,5.06815916886402,4.70461330559735,4.12186028379493,5.52687639468169,4.54759222552077,6.99983837082817,5.30971462002893,3.46335272233694,5.22000001822073],"arrayminus":[4.47715615918023,4.87629270306697,5.54088845026394,4.75127266783613,4.20964567999614,5.19344169579827,3.13788381396218,5.91098130172079,6.31902476858055,5.80926247644601,5.06815916886402,4.70461330559735,4.12186028379493,5.52687639468169,4.54759222552077,6.99983837082817,5.30971462002893,3.46335272233694,5.22000001822073],"type":"data","width":1.01311623699693,"symmetric":false,"color":"rgba(0,0,0,1)"},"frame":null}],"layout":{"margin":{"t":26.2283105022831,"r":7.30593607305936,"b":40.1826484018265,"l":43.1050228310502},"plot_bgcolor":"rgba(235,235,235,1)","paper_bgcolor":"rgba(255,255,255,1)","font":{"color":"rgba(0,0,0,1)","family":"","size":14.6118721461187},"xaxis":{"domain":[0,1],"automargin":true,"type":"linear","autorange":false,"range":[1780.505,1979.495],"tickmode":"array","ticktext":["1800","1850","1900","1950"],"tickvals":[1800,1850,1900,1950],"categoryorder":"array","categoryarray":["1800","1850","1900","1950"],"nticks":null,"ticks":"outside","tickcolor":"rgba(51,51,51,1)","ticklen":3.65296803652968,"tickwidth":0.66417600664176,"showticklabels":true,"tickfont":{"color":"rgba(77,77,77,1)","family":"","size":11.689497716895},"tickangle":-0,"showline":false,"linecolor":null,"linewidth":0,"showgrid":true,"gridcolor":"rgba(255,255,255,1)","gridwidth":0.66417600664176,"zeroline":false,"anchor":"y","title":{"text":"Year","font":{"color":"rgba(0,0,0,1)","family":"","size":14.6118721461187}},"hoverformat":".2f"},"yaxis":{"domain":[0,1],"automargin":true,"type":"linear","autorange":false,"range":[-10.9955139680503,218.868357827091],"tickmode":"array","ticktext":["0","50","100","150","200"],"tickvals":[0,50,100,150,200],"categoryorder":"array","categoryarray":["0","50","100","150","200"],"nticks":null,"ticks":"outside","tickcolor":"rgba(51,51,51,1)","ticklen":3.65296803652968,"tickwidth":0.66417600664176,"showticklabels":true,"tickfont":{"color":"rgba(77,77,77,1)","family":"","size":11.689497716895},"tickangle":-0,"showline":false,"linecolor":null,"linewidth":0,"showgrid":true,"gridcolor":"rgba(255,255,255,1)","gridwidth":0.66417600664176,"zeroline":false,"anchor":"x","title":{"text":"Population","font":{"color":"rgba(0,0,0,1)","family":"","size":14.6118721461187}},"hoverformat":".2f"},"shapes":[{"type":"rect","fillcolor":null,"line":{"color":null,"width":0,"linetype":[]},"yref":"paper","xref":"paper","x0":0,"x1":1,"y0":0,"y1":1}],"showlegend":false,"legend":{"bgcolor":"rgba(255,255,255,1)","bordercolor":"transparent","borderwidth":1.88976377952756,"font":{"color":"rgba(0,0,0,1)","family":"","size":11.689497716895}},"hovermode":"closest","barmode":"relative"},"config":{"doubleClick":"reset","showSendToCloud":false},"source":"A","attrs":{"7661413daaa1":{"x":{},"y":{},"ymin":{},"ymax":{},"type":"scatter"},"7661748583e6":{"x":{},"y":{},"ymin":{},"ymax":{}},"76613402f390":{"x":{},"y":{},"ymin":{},"ymax":{}}},"cur_data":"7661413daaa1","visdat":{"7661413daaa1":["function (y) ","x"],"7661748583e6":["function (y) ","x"],"76613402f390":["function (y) ","x"]},"highlight":{"on":"plotly_click","persistent":false,"dynamic":false,"selectize":false,"opacityDim":0.2,"selected":{"opacity":1},"debounce":0},"shinyEvents":["plotly_hover","plotly_click","plotly_selected","plotly_relayout","plotly_brushed","plotly_brushing","plotly_clickannotation","plotly_doubleclick","plotly_deselect","plotly_afterplot","plotly_sunburstclick"],"base_url":"https://plot.ly"},"evals":[],"jsHooks":[]}</script>

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
