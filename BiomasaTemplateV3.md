---
title: "BiomasAnalysisV3"
author: "Gabriela Lopez"
date: "Friday, February 13, 2015"
output: html_document
---
**Requierements for using the ForestPlots.net Report template** 

(This section can be deleted once you're ready to publish your report)
Sofware requirements

This is a template to produce an html document that reports above-ground biomass (AGB), stem density, wood mass density estimates and frequency and number of species by Family.
You will need to install R and RStudio in your computer to modify and run the template.

The template is an R Markdown docuemnt that can be modified by ForestPlots.net users. For more details on using R Markdown see <http://rmarkdown.rstudio.com>. 
Clicking **Knit** button will generate a the docoument.

The template needs the following packages: a) BiomasaFP (package for estimating biomass and other forest parameters from data donwloaded from ForestPlots.net ); 


**Data requirements**
You need to download 3 files from ForestPlots.net:  a) Individuals csv file from the Advanced Search, b) Wood density file  from the query library and c) Plot View metadata file from the query library. The 3 files should correspond to the same Plot Views. The 3 files should be saved in the same working directory.

**Instructions**
Text in italics should be updated according to the dataset you're using. 

**Introduction**

This document summarizes Forest Inventory Data collected by the *RAINFOR network (www.rainfor.org)*.  The plots (plotviews) in this report conform to the following criteria: *multiple census plots*, *minimum diameter of 100mm*, *plot area greater than 0.2 ha*.

This document reports: a) Aboveground biomass (AGB), b) Basal Area (BA), c) wood density and d) frequency and number of species by Family for each Plot View.

-----
**Data processing**

The data was downloaded from ForestPlots.net (Lopez-Gonzalez et al., 2011; Lopez-Gonzalez et al., 2009) on *date*. The plots included in this report can be found in the table below. 

Note: click on a column header to sort the rows.

**Table 1. Plots included in this report**








<!-- Table generated in R 3.1.2 by googleVis 0.5.8 package -->
<!-- Sat Feb 14 00:32:01 2015 -->


<!-- jsHeader -->
<script type="text/javascript">
 
// jsData 
function gvisDataTableID1eb02901d44 () {
var data = new google.visualization.DataTable();
var datajson =
[
 [
 "PERU",
"CUZ-01",
40,
-12.53783,
-69.05993,
1989.389,
2014.729,
8 
],
[
 "PERU",
"CUZ-02",
41,
-12.53992,
-69.05783,
1989.4,
2014.726,
8 
],
[
 "PERU",
"MNU-01",
1121,
-11.88748,
-71.40596,
1990.704,
2010.704,
5 
],
[
 "PERU",
"MNU-05",
70,
-11.87849,
-71.40863,
1989.781,
2012.6095,
7 
],
[
 "PERU",
"PNY-04",
707,
-10.34121,
-75.2529,
2007.547,
2011.822,
3 
],
[
 "VENEZUELA",
"BAC-01",
971,
7.46322,
-71.01307,
1991.279,
2012.104,
12 
],
[
 "VENEZUELA",
"CBN-06",
36,
8.58333,
-71.41667,
1961.521,
1985.8,
23 
] 
];
data.addColumn('string','Country');
data.addColumn('string','PlotCode');
data.addColumn('number','PlotViewID');
data.addColumn('number','LatitudeDecimal');
data.addColumn('number','LongitudeDecimal');
data.addColumn('number','First.Census.Date');
data.addColumn('number','Last.Census.Date');
data.addColumn('number','No.Censuses');
data.addRows(datajson);
return(data);
}
 
// jsDrawChart
function drawChartTableID1eb02901d44() {
var data = gvisDataTableID1eb02901d44();
var options = {};
options["allowHtml"] = true;

    var chart = new google.visualization.Table(
    document.getElementById('TableID1eb02901d44')
    );
    chart.draw(data,options);
    

}
  
 
// jsDisplayChart
(function() {
var pkgs = window.__gvisPackages = window.__gvisPackages || [];
var callbacks = window.__gvisCallbacks = window.__gvisCallbacks || [];
var chartid = "table";
  
// Manually see if chartid is in pkgs (not all browsers support Array.indexOf)
var i, newPackage = true;
for (i = 0; newPackage && i < pkgs.length; i++) {
if (pkgs[i] === chartid)
newPackage = false;
}
if (newPackage)
  pkgs.push(chartid);
  
// Add the drawChart function to the global list of callbacks
callbacks.push(drawChartTableID1eb02901d44);
})();
function displayChartTableID1eb02901d44() {
  var pkgs = window.__gvisPackages = window.__gvisPackages || [];
  var callbacks = window.__gvisCallbacks = window.__gvisCallbacks || [];
  window.clearTimeout(window.__gvisLoad);
  // The timeout is set to 100 because otherwise the container div we are
  // targeting might not be part of the document yet
  window.__gvisLoad = setTimeout(function() {
  var pkgCount = pkgs.length;
  google.load("visualization", "1", { packages:pkgs, callback: function() {
  if (pkgCount != pkgs.length) {
  // Race condition where another setTimeout call snuck in after us; if
  // that call added a package, we must not shift its callback
  return;
}
while (callbacks.length > 0)
callbacks.shift()();
} });
}, 100);
}
 
// jsFooter
</script>
 
<!-- jsChart -->  
<script type="text/javascript" src="https://www.google.com/jsapi?callback=displayChartTableID1eb02901d44"></script>
 
<!-- divChart -->
  
<div id="TableID1eb02901d44" 
  style="width: 500; height: automatic;">
</div>


The plot location is shown in the map in Figure 1.

**Figure 1. Map of Plot Location**

<!-- Map generated in R 3.1.2 by googleVis 0.5.8 package -->
<!-- Sat Feb 14 00:32:01 2015 -->


<!-- jsHeader -->
<script type="text/javascript">
 
// jsData 
function gvisDataMapID1eb014d498a () {
var data = new google.visualization.DataTable();
var datajson =
[
 [
 -12.53783,
-69.05993,
"CUZ-01" 
],
[
 -12.53992,
-69.05783,
"CUZ-02" 
],
[
 -11.88748,
-71.40596,
"MNU-01" 
],
[
 -11.87849,
-71.40863,
"MNU-05" 
],
[
 -10.34121,
-75.2529,
"PNY-04" 
],
[
 7.46322,
-71.01307,
"BAC-01" 
],
[
 8.58333,
-71.41667,
"CBN-06" 
] 
];
data.addColumn('number','Latitude');
data.addColumn('number','Longitude');
data.addColumn('string','PlotCode');
data.addRows(datajson);
return(data);
}
 
// jsDrawChart
function drawChartMapID1eb014d498a() {
var data = gvisDataMapID1eb014d498a();
var options = {};
options["showTip"] = true;
options["enableScrollWheel"] = true;
options["useMapTypeControl"] = true;
options["width"] =    600;
options["height"] =    400;
options["dataMode"] = "markers";

    var chart = new google.visualization.Map(
    document.getElementById('MapID1eb014d498a')
    );
    chart.draw(data,options);
    

}
  
 
// jsDisplayChart
(function() {
var pkgs = window.__gvisPackages = window.__gvisPackages || [];
var callbacks = window.__gvisCallbacks = window.__gvisCallbacks || [];
var chartid = "map";
  
// Manually see if chartid is in pkgs (not all browsers support Array.indexOf)
var i, newPackage = true;
for (i = 0; newPackage && i < pkgs.length; i++) {
if (pkgs[i] === chartid)
newPackage = false;
}
if (newPackage)
  pkgs.push(chartid);
  
// Add the drawChart function to the global list of callbacks
callbacks.push(drawChartMapID1eb014d498a);
})();
function displayChartMapID1eb014d498a() {
  var pkgs = window.__gvisPackages = window.__gvisPackages || [];
  var callbacks = window.__gvisCallbacks = window.__gvisCallbacks || [];
  window.clearTimeout(window.__gvisLoad);
  // The timeout is set to 100 because otherwise the container div we are
  // targeting might not be part of the document yet
  window.__gvisLoad = setTimeout(function() {
  var pkgCount = pkgs.length;
  google.load("visualization", "1", { packages:pkgs, callback: function() {
  if (pkgCount != pkgs.length) {
  // Race condition where another setTimeout call snuck in after us; if
  // that call added a package, we must not shift its callback
  return;
}
while (callbacks.length > 0)
callbacks.shift()();
} });
}, 100);
}
 
// jsFooter
</script>
 
<!-- jsChart -->  
<script type="text/javascript" src="https://www.google.com/jsapi?callback=displayChartMapID1eb014d498a"></script>
 
<!-- divChart -->
  
<div id="MapID1eb014d498a" 
  style="width: 600; height: 400;">
</div>

**Results**
Table 2 shows the Aboveground Biomass estimated using Chave (2005) Moist forest equation with heigt and wood density as parameters.Height was estimated using regional parameters  for a Weibull model (Feldpaush, 2011). 

**Table 2 Aboveground Biomass by PlotViewID and Census**
<!-- Table generated in R 3.1.2 by googleVis 0.5.8 package -->
<!-- Sat Feb 14 00:32:03 2015 -->


<!-- jsHeader -->
<script type="text/javascript">
 
// jsData 
function gvisDataTableID1eb072277b88 () {
var data = new google.visualization.DataTable();
var datajson =
[
 [
 36,
1,
"VENEZUELA",
"CBN-06",
0.25,
8.58333,
-71.41667,
1961.521,
366.7640584,
364 
],
[
 36,
2,
"VENEZUELA",
"CBN-06",
0.25,
8.58333,
-71.41667,
1962.521,
367.4815011,
364 
],
[
 36,
3,
"VENEZUELA",
"CBN-06",
0.25,
8.58333,
-71.41667,
1963.521,
368.3669326,
364 
],
[
 36,
4,
"VENEZUELA",
"CBN-06",
0.25,
8.58333,
-71.41667,
1964.519,
358.0003938,
356 
],
[
 36,
5,
"VENEZUELA",
"CBN-06",
0.25,
8.58333,
-71.41667,
1965.521,
355.5827909,
352 
],
[
 36,
6,
"VENEZUELA",
"CBN-06",
0.25,
8.58333,
-71.41667,
1966.521,
349.003079,
336 
],
[
 36,
7,
"VENEZUELA",
"CBN-06",
0.25,
8.58333,
-71.41667,
1967.521,
386.2420425,
652 
],
[
 36,
8,
"VENEZUELA",
"CBN-06",
0.25,
8.58333,
-71.41667,
1968.601,
388.1675804,
668 
],
[
 36,
9,
"VENEZUELA",
"CBN-06",
0.25,
8.58333,
-71.41667,
1969.441,
388.6176444,
664 
],
[
 36,
10,
"VENEZUELA",
"CBN-06",
0.25,
8.58333,
-71.41667,
1970.54,
392.2292897,
664 
],
[
 36,
11,
"VENEZUELA",
"CBN-06",
0.25,
8.58333,
-71.41667,
1971.521,
388.0787125,
664 
],
[
 36,
12,
"VENEZUELA",
"CBN-06",
0.25,
8.58333,
-71.41667,
1972.53,
390.3560705,
672 
],
[
 36,
13,
"VENEZUELA",
"CBN-06",
0.25,
8.58333,
-71.41667,
1973.501,
380.3053207,
648 
],
[
 36,
14,
"VENEZUELA",
"CBN-06",
0.25,
8.58333,
-71.41667,
1974.521,
382.2286567,
668 
],
[
 36,
15,
"VENEZUELA",
"CBN-06",
0.25,
8.58333,
-71.41667,
1975.729,
386.4818143,
668 
],
[
 36,
16,
"VENEZUELA",
"CBN-06",
0.25,
8.58333,
-71.41667,
1976.74,
385.2840456,
676 
],
[
 36,
17,
"VENEZUELA",
"CBN-06",
0.25,
8.58333,
-71.41667,
1977.921,
347.7631237,
660 
],
[
 36,
18,
"VENEZUELA",
"CBN-06",
0.25,
8.58333,
-71.41667,
1978.951,
348.7631095,
656 
],
[
 36,
19,
"VENEZUELA",
"CBN-06",
0.25,
8.58333,
-71.41667,
1979.759,
350.2250753,
652 
],
[
 36,
20,
"VENEZUELA",
"CBN-06",
0.25,
8.58333,
-71.41667,
1980.77,
349.2444923,
640 
],
[
 36,
21,
"VENEZUELA",
"CBN-06",
0.25,
8.58333,
-71.41667,
1981.819,
341.7170965,
636 
],
[
 36,
22,
"VENEZUELA",
"CBN-06",
0.25,
8.58333,
-71.41667,
1984.47,
316.5767797,
612 
],
[
 36,
23,
"VENEZUELA",
"CBN-06",
0.25,
8.58333,
-71.41667,
1985.8,
318.4607188,
616 
],
[
 40,
1,
"PERU",
"CUZ-01",
1,
-12.53783,
-69.05993,
1989.389,
231.744767,
489 
],
[
 40,
2,
"PERU",
"CUZ-01",
1,
-12.53783,
-69.05993,
1994.622,
247.602635,
516 
],
[
 40,
3,
"PERU",
"CUZ-01",
1,
-12.53783,
-69.05993,
1998.77,
262.2257433,
534 
],
[
 40,
4,
"PERU",
"CUZ-01",
1,
-12.53783,
-69.05993,
2003.74,
265.3718327,
527 
],
[
 40,
5,
"PERU",
"CUZ-01",
1,
-12.53783,
-69.05993,
2006.649,
248.0748103,
441 
],
[
 40,
6,
"PERU",
"CUZ-01",
1,
-12.53783,
-69.05993,
2008.678,
236.2384648,
435 
],
[
 40,
7,
"PERU",
"CUZ-01",
1,
-12.53783,
-69.05993,
2011.69,
240.2277154,
489 
],
[
 40,
8,
"PERU",
"CUZ-01",
1,
-12.53783,
-69.05993,
2014.729,
252.3181243,
426 
],
[
 41,
1,
"PERU",
"CUZ-02",
1,
-12.53992,
-69.05783,
1989.4,
212.4518794,
509 
],
[
 41,
2,
"PERU",
"CUZ-02",
1,
-12.53992,
-69.05783,
1994.619,
229.1785772,
525 
],
[
 41,
3,
"PERU",
"CUZ-02",
1,
-12.53992,
-69.05783,
1998.77,
235.9539344,
539 
],
[
 41,
4,
"PERU",
"CUZ-02",
1,
-12.53992,
-69.05783,
2003.751,
236.7028719,
558 
],
[
 41,
5,
"PERU",
"CUZ-02",
1,
-12.53992,
-69.05783,
2006.63,
242.899479,
554 
],
[
 41,
6,
"PERU",
"CUZ-02",
1,
-12.53992,
-69.05783,
2008.689,
248.6404234,
555 
],
[
 41,
7,
"PERU",
"CUZ-02",
1,
-12.53992,
-69.05783,
2011.685,
255.8372505,
537 
],
[
 41,
8,
"PERU",
"CUZ-02",
1,
-12.53992,
-69.05783,
2014.726,
237.6748725,
508 
],
[
 70,
1,
"PERU",
"MNU-05",
2,
-11.87849,
-71.40863,
1989.781,
332.2757576,
593 
],
[
 70,
2,
"PERU",
"MNU-05",
2,
-11.87849,
-71.40863,
1990.781,
337.4495348,
603.5 
],
[
 70,
3,
"PERU",
"MNU-05",
2,
-11.87849,
-71.40863,
1994.781,
341.5178988,
628.5 
],
[
 70,
4,
"PERU",
"MNU-05",
2,
-11.87849,
-71.40863,
2000.224,
352.2971706,
629 
],
[
 70,
5,
"PERU",
"MNU-05",
2,
-11.87849,
-71.40863,
2004.699,
333.3127029,
610.5 
],
[
 70,
6,
"PERU",
"MNU-05",
2,
-11.87849,
-71.40863,
2008.639,
331.0494433,
617.5 
],
[
 70,
7,
"PERU",
"MNU-05",
2,
-11.87849,
-71.40863,
2012.6095,
338.583016,
634.5 
],
[
 707,
1,
"PERU",
"PNY-04",
1,
-10.34121,
-75.2529,
2007.547,
213.8307648,
575 
],
[
 707,
2,
"PERU",
"PNY-04",
1,
-10.34121,
-75.2529,
2009.715,
208.3763679,
543 
],
[
 707,
3,
"PERU",
"PNY-04",
1,
-10.34121,
-75.2529,
2011.822,
205.8893748,
523 
],
[
 971,
1,
"VENEZUELA",
"BAC-01",
0.25,
7.46322,
-71.01307,
1991.279,
165.9706782,
308 
],
[
 971,
2,
"VENEZUELA",
"BAC-01",
0.25,
7.46322,
-71.01307,
1991.86,
169.3903966,
312 
],
[
 971,
3,
"VENEZUELA",
"BAC-01",
0.25,
7.46322,
-71.01307,
1992.459,
173.5292837,
316 
],
[
 971,
4,
"VENEZUELA",
"BAC-01",
0.25,
7.46322,
-71.01307,
1996.309,
177.098052,
304 
],
[
 971,
5,
"VENEZUELA",
"BAC-01",
0.25,
7.46322,
-71.01307,
2001.249,
172.0732935,
300 
],
[
 971,
6,
"VENEZUELA",
"BAC-01",
0.25,
7.46322,
-71.01307,
2002.359,
176.3551423,
280 
],
[
 971,
7,
"VENEZUELA",
"BAC-01",
0.25,
7.46322,
-71.01307,
2004.079,
187.2497014,
276 
],
[
 971,
8,
"VENEZUELA",
"BAC-01",
0.25,
7.46322,
-71.01307,
2005.151,
188.6925329,
264 
],
[
 971,
9,
"VENEZUELA",
"BAC-01",
0.25,
7.46322,
-71.01307,
2006.17,
190.8549665,
256 
],
[
 971,
10,
"VENEZUELA",
"BAC-01",
0.25,
7.46322,
-71.01307,
2007.31,
194.8936791,
244 
],
[
 971,
11,
"VENEZUELA",
"BAC-01",
0.25,
7.46322,
-71.01307,
2009.14,
202.9830864,
240 
],
[
 971,
12,
"VENEZUELA",
"BAC-01",
0.25,
7.46322,
-71.01307,
2012.104,
202.7736722,
252 
],
[
 1121,
1,
"PERU",
"MNU-01",
2.25,
-11.88748,
-71.40596,
1990.704,
292.751514,
572 
],
[
 1121,
2,
"PERU",
"MNU-01",
2.25,
-11.88748,
-71.40596,
1995.704,
287.8301699,
580.8888889 
],
[
 1121,
3,
"PERU",
"MNU-01",
2.25,
-11.88748,
-71.40596,
2000.705,
296.63588,
569.3333333 
],
[
 1121,
4,
"PERU",
"MNU-01",
2.25,
-11.88748,
-71.40596,
2005.704,
307.1541363,
580 
],
[
 1121,
5,
"PERU",
"MNU-01",
2.25,
-11.88748,
-71.40596,
2010.704,
315.8057805,
588.4444444 
] 
];
data.addColumn('number','PlotViewID');
data.addColumn('number','Census.No');
data.addColumn('string','CountryName');
data.addColumn('string','PlotCode');
data.addColumn('number','PlotArea');
data.addColumn('number','LatitudeDecimal');
data.addColumn('number','LongitudeDecimal');
data.addColumn('number','Census.Mean.Date');
data.addColumn('number','AGB_ha');
data.addColumn('number','No.AliveInd_ha');
data.addRows(datajson);
return(data);
}
 
// jsDrawChart
function drawChartTableID1eb072277b88() {
var data = gvisDataTableID1eb072277b88();
var options = {};
options["allowHtml"] = true;
options["page"] = "enable";

    var chart = new google.visualization.Table(
    document.getElementById('TableID1eb072277b88')
    );
    chart.draw(data,options);
    

}
  
 
// jsDisplayChart
(function() {
var pkgs = window.__gvisPackages = window.__gvisPackages || [];
var callbacks = window.__gvisCallbacks = window.__gvisCallbacks || [];
var chartid = "table";
  
// Manually see if chartid is in pkgs (not all browsers support Array.indexOf)
var i, newPackage = true;
for (i = 0; newPackage && i < pkgs.length; i++) {
if (pkgs[i] === chartid)
newPackage = false;
}
if (newPackage)
  pkgs.push(chartid);
  
// Add the drawChart function to the global list of callbacks
callbacks.push(drawChartTableID1eb072277b88);
})();
function displayChartTableID1eb072277b88() {
  var pkgs = window.__gvisPackages = window.__gvisPackages || [];
  var callbacks = window.__gvisCallbacks = window.__gvisCallbacks || [];
  window.clearTimeout(window.__gvisLoad);
  // The timeout is set to 100 because otherwise the container div we are
  // targeting might not be part of the document yet
  window.__gvisLoad = setTimeout(function() {
  var pkgCount = pkgs.length;
  google.load("visualization", "1", { packages:pkgs, callback: function() {
  if (pkgCount != pkgs.length) {
  // Race condition where another setTimeout call snuck in after us; if
  // that call added a package, we must not shift its callback
  return;
}
while (callbacks.length > 0)
callbacks.shift()();
} });
}, 100);
}
 
// jsFooter
</script>
 
<!-- jsChart -->  
<script type="text/javascript" src="https://www.google.com/jsapi?callback=displayChartTableID1eb072277b88"></script>
 
<!-- divChart -->
  
<div id="TableID1eb072277b88" 
  style="width: automatic; height: automatic;">
</div>


Aboveground biomass change was estimated as the difference in AGB between the first and last census, divided by the time elapsed (Figure 3). In Figure 3 biomass change is indicated by colour and the size of the marker represents the AGB weighted mean.

**Figure 3. Map of Change**

Note: This type of map includes an option for selecting region. In the configuration options of the following you can find the region codes: link https://developers.google.com/chart/interactive/docs/gallery/geomap
<!-- GeoChart generated in R 3.1.2 by googleVis 0.5.8 package -->
<!-- Sat Feb 14 00:32:05 2015 -->


<!-- jsHeader -->
<script type="text/javascript">
 
// jsData 
function gvisDataGeoChartID1eb02a1ce3c () {
var data = new google.visualization.DataTable();
var datajson =
[
 [
 8.58333,
-71.41667,
-1.989511083,
365.4349014 
],
[
 -12.53783,
-69.05993,
0.8118925536,
247.9813738 
],
[
 -12.53992,
-69.05783,
0.9959327594,
237.4586493 
],
[
 -11.87849,
-71.40863,
0.2762887783,
338.0674742 
],
[
 -10.34121,
-75.2529,
-1.857635095,
209.362682 
],
[
 7.46322,
-71.01307,
1.767250616,
183.526914 
],
[
 -11.88748,
-71.40596,
1.152713326,
300.0682005 
] 
];
data.addColumn('number','Latitude');
data.addColumn('number','Longitude');
data.addColumn('number','AGBChangeyr');
data.addColumn('number','AGBWeightedMean');
data.addRows(datajson);
return(data);
}
 
// jsDrawChart
function drawChartGeoChartID1eb02a1ce3c() {
var data = gvisDataGeoChartID1eb02a1ce3c();
var options = {};
options["width"] =    600;
options["height"] =    400;
options["enableScrollWheel"] = true;
options["useMapTypeControl"] = true;
options["region"] = "005";
options["dataMode"] = "markers";

    var chart = new google.visualization.GeoChart(
    document.getElementById('GeoChartID1eb02a1ce3c')
    );
    chart.draw(data,options);
    

}
  
 
// jsDisplayChart
(function() {
var pkgs = window.__gvisPackages = window.__gvisPackages || [];
var callbacks = window.__gvisCallbacks = window.__gvisCallbacks || [];
var chartid = "geochart";
  
// Manually see if chartid is in pkgs (not all browsers support Array.indexOf)
var i, newPackage = true;
for (i = 0; newPackage && i < pkgs.length; i++) {
if (pkgs[i] === chartid)
newPackage = false;
}
if (newPackage)
  pkgs.push(chartid);
  
// Add the drawChart function to the global list of callbacks
callbacks.push(drawChartGeoChartID1eb02a1ce3c);
})();
function displayChartGeoChartID1eb02a1ce3c() {
  var pkgs = window.__gvisPackages = window.__gvisPackages || [];
  var callbacks = window.__gvisCallbacks = window.__gvisCallbacks || [];
  window.clearTimeout(window.__gvisLoad);
  // The timeout is set to 100 because otherwise the container div we are
  // targeting might not be part of the document yet
  window.__gvisLoad = setTimeout(function() {
  var pkgCount = pkgs.length;
  google.load("visualization", "1", { packages:pkgs, callback: function() {
  if (pkgCount != pkgs.length) {
  // Race condition where another setTimeout call snuck in after us; if
  // that call added a package, we must not shift its callback
  return;
}
while (callbacks.length > 0)
callbacks.shift()();
} });
}, 100);
}
 
// jsFooter
</script>
 
<!-- jsChart -->  
<script type="text/javascript" src="https://www.google.com/jsapi?callback=displayChartGeoChartID1eb02a1ce3c"></script>
 
<!-- divChart -->
  
<div id="GeoChartID1eb02a1ce3c" 
  style="width: 600; height: 400;">
</div>

**References**

Chave J, Coomes DA, Jansen S, Lewis SL, Swenson NG, Zanne AE. 2009. Towards a worldwide wood economics spectrum. Ecology Letters 12(4): 351-366. http://dx.doi.org/10.1111/j.1461-0248.2009.01285.x

Chave C, Andalo S, Brown, et al. 2005. Tree allometry and improved estimation of carbon stocks and balance in tropical forests. Oecologia 145 (1):87-99. doi:10.1007/s00442-005-0100-x.

Chave J, Rejou-Mechain M, Burquez A et al. 2014. Improved allometric models to estimate the aboveground biomass of tropical trees. Global Change Biology 20: 3177-3190. doi: 10.1111/gcb.12629

Feldpausch TR, Banin L, Phillips OL, Baker TR, Lewis SL et al. 2011. Height-diameter allometry of tropical forest trees. Biogeosciences 8 (5):1081-1106. doi:10.5194/bg-8-1081-2011.

Lopez-Gonzalez  G. (2014). BiomasaFP: Estimates Biomass for data dowloaded from ForestPlots.net. R package version 1.0.

Lopez-Gonzalez, G., Lewis, S.L., Burkitt, M. and Phillips, O.L. (2011). ForestPlots.net: a web application and research tool to manage and analyse tropical forest plot data. Journal of Vegetation Science 22: 610–613. doi: 10.1111/j.1654-1103.2011.01312.x

Lopez-Gonzalez, G., Lewis, S.L., Burkitt, M., Baker T.R. and Phillips, O.L. (2009). ForestPlots.net Database. www.forestplots.net. Date of extraction *[dd,mm,yy]*.

R Core Team (2014). R: A language and environment for statistical computing. R Foundation for Statistical Computing, Vienna, Austria. URL http://www.R-project.org/.

Zanne AE, Lopez-Gonzalez G, Coomes DA, Ilic J, Jansen S, Lewis SL, Miller RB, Swenson NG, Wiemann MC, Chave J. 2009. Data from: Towards a worldwide wood economics spectrum. Dryad Digital Repository. http://dx.doi.org/10.5061/dryad.234
