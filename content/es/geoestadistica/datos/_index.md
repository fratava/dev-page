---
# Title, summary, and page position.
linktitle: datos
summary: Datos
weight: 8
icon: database
icon_pack: fas

# Page metadata.
title: Datos
date: "2021-03-12T00:00:00Z"
type: book  # Do not modify.
---

## Daily rainfall measurements for Italy (2010)

### Dataset 

<iframe src="https://drive.google.com/embeddedfolderview?id=1MzdN0-XiaG84MFYwIKocpA7HqXWyljNV#grid" style="width:100%; height:600px; border:0;"></iframe>

### Bibliografía

El artículo se puede encontrar en la página 189. Ahí se describe a detalle cada columna del archivo .CSV y se muestran gráficas del semiovarigrama, estadísticos, etc.

<iframe src="https://drive.google.com/embeddedfolderview?id=1VM3BywZlTLzJjae5FB5SK6osdXYXQpLM#grid" style="width:100%; height:600px; border:0;"></iframe>


## Boston Housing 1970s

### Dataset

<iframe src="https://drive.google.com/embeddedfolderview?id=1wL41Ud_p0Z5SvfrURQvV-pvalNuV_EeM#grid" style="width:100%; height:600px; border:0;"></iframe>

### Description

<!DOCTYPE html PUBLIC "-//W3C//DTD HTML 4.01//EN" "http://www.w3.org/TR/html4/strict.dtd">
<html>
<head>
  <meta http-equiv="Content-Type" content="text/html; charset=utf-8">
  <meta http-equiv="Content-Style-Type" content="text/css">
  <title>Boston Housing Data</title>
  <meta name="Generator" content="Cocoa HTML Writer">
  <meta name="CocoaVersion" content="1348.17">
  <style type="text/css">
    p.p2 {margin: 0.0px 0.0px 12.0px 0.0px; font: 12.0px Times; color: #000000; -webkit-text-stroke: #000000}
    p.p3 {margin: 0.0px 0.0px 6.0px 0.0px; font: 12.0px Times; color: #000000; -webkit-text-stroke: #000000; min-height: 14.0px}
    p.p4 {margin: 0.0px 0.0px 0.0px 0.0px; font: 12.0px Times; color: #000000; -webkit-text-stroke: #000000}
    p.p5 {margin: 0.0px 0.0px 0.0px 0.0px; text-align: center; font: 12.0px Times; color: #000000; -webkit-text-stroke: #000000}
    p.p6 {margin: 0.0px 0.0px 0.0px 0.0px; font: 12.0px Times; color: #000000; -webkit-text-stroke: #000000; min-height: 14.0px}
    span.s1 {font-kerning: none}
    span.s2 {font: 12.0px Times; text-decoration: underline ; font-kerning: none; color: #0000ee; -webkit-text-stroke: 0px #0000ee}
    td.td1 {width: 94.0px; margin: 0.5px 0.5px 0.5px 0.5px; padding: 1.0px 1.0px 1.0px 1.0px}
    td.td2 {width: 199.0px; margin: 0.5px 0.5px 0.5px 0.5px; padding: 1.0px 1.0px 1.0px 1.0px}
    td.td3 {width: 54.0px; margin: 0.5px 0.5px 0.5px 0.5px; padding: 1.0px 1.0px 1.0px 1.0px}
    td.td4 {width: 592.0px; margin: 0.5px 0.5px 0.5px 0.5px; padding: 1.0px 1.0px 1.0px 1.0px}
  </style>
</head>
<body>
<h1 style="margin: 0.0px 0.0px 16.1px 0.0px; font: 24.0px Times; color: #000000; -webkit-text-stroke: #000000"><span class="s1"><b>Boston Housing Data</b></span></h1>
<p class="p2"><span class="s1"><b>File Description</b><br>
Housing and neighborhood data for the city of Boston.</span></p>

<p class="p2"><span class="s1">Observations = 506<br>
Variables = 23</span></p>

<p class="p2"><span class="s1"><b>Source</b><br>
Data created from boston.c data frame in R's spdep package. Original source: <a href="http://lib.stat.cmu.edu/datasets/boston_corrected.txt"><span class="s2">http://lib.stat.cmu.edu/datasets/boston_corrected.txt</span></a><br>
Variables and References: R spdep Manual (p. 15), available at <a href="http://cran.us.r-project.org/"><span class="s2">http://cran.us.r-project.org</span></a></span></p>

<p class="p2"><span class="s1"><b>References</b><br>
Harrison, David, and Daniel L. Rubinfeld. (1978). Hedonic Housing Prices and the Demand for Clean Air, <i>Journal of Environmental Economics and Management</i>, Volume 5, 81- 102. Original data.</span></p>
<p class="p2"><span class="s1">Gilley, O.W., and R. Kelley Pace. (1996). On the Harrison and Rubinfeld Data, <i>Journal of Environmental Economics and Management</i>, 31, 403-405. Provided corrections and examined censoring.</span></p>
<p class="p2"><span class="s1">Pace, R. Kelley, and O.W. Gilley. (1997). Using the Spatial Configuration of the Data to Improve Estimation, <i>Journal of the Real Estate Finance and Economics</i>, 14, 333-340.</span></p>
<table cellspacing="0" cellpadding="0">
  <tbody>
    <tr>
      <td valign="middle" class="td3">
        <p class="p5"><span class="s1"><b>Variable</b></span></p>
      </td>
      <td valign="middle" class="td4">
        <p class="p5"><span class="s1"><b>Description</b></span></p>
      </td>
    </tr>
    <tr>
      <td valign="middle" class="td3">
        <p class="p4"><span class="s1">ID<span class="Apple-converted-space"> </span></span></p>
      </td>
      <td valign="middle" class="td4">
        <p class="p4"><span class="s1">Sequential ID<span class="Apple-converted-space"> </span></span></p>
      </td>
    </tr>
    <tr>
      <td valign="middle" class="td3">
        <p class="p4"><span class="s1">TOWN<span class="Apple-converted-space"> </span></span></p>
      </td>
      <td valign="middle" class="td4">
        <p class="p4"><span class="s1">A factor with levels given by town names<span class="Apple-converted-space"> </span></span></p>
      </td>
    </tr>
    <tr>
      <td valign="middle" class="td3">
        <p class="p4"><span class="s1">TOWNNO<span class="Apple-converted-space"> </span></span></p>
      </td>
      <td valign="middle" class="td4">
        <p class="p4"><span class="s1">A numeric vector corresponding to TOWN<span class="Apple-converted-space"> </span></span></p>
      </td>
    </tr>
    <tr>
      <td valign="middle" class="td3">
        <p class="p4"><span class="s1">TRACT<span class="Apple-converted-space"> </span></span></p>
      </td>
      <td valign="middle" class="td4">
        <p class="p4"><span class="s1">A numeric vector of tract ID numbers<span class="Apple-converted-space"> </span></span></p>
      </td>
    </tr>
    <tr>
      <td valign="middle" class="td3">
        <p class="p4"><span class="s1">LON<span class="Apple-converted-space"> </span></span></p>
      </td>
      <td valign="middle" class="td4">
        <p class="p4"><span class="s1">A numeric vector of tract point longitudes in decimal degrees<span class="Apple-converted-space"> </span></span></p>
      </td>
    </tr>
    <tr>
      <td valign="middle" class="td3">
        <p class="p4"><span class="s1">LAT<span class="Apple-converted-space"> </span></span></p>
      </td>
      <td valign="middle" class="td4">
        <p class="p4"><span class="s1">A numeric vector of tract point latitudes in decimal degrees<span class="Apple-converted-space"> </span></span></p>
      </td>
    </tr>
    <tr>
      <td valign="middle" class="td3">
        <p class="p4"><span class="s1">X<span class="Apple-converted-space"> </span></span></p>
      </td>
      <td valign="middle" class="td4">
        <p class="p4"><span class="s1">X Coordinates (UTM Zone 19)<span class="Apple-converted-space"> </span></span></p>
      </td>
    </tr>
    <tr>
      <td valign="middle" class="td3">
        <p class="p4"><span class="s1">Y<span class="Apple-converted-space"> </span></span></p>
      </td>
      <td valign="middle" class="td4">
        <p class="p4"><span class="s1">Y Coordinates (UTM Zone 19)<span class="Apple-converted-space"> </span></span></p>
      </td>
    </tr>
    <tr>
      <td valign="middle" class="td3">
        <p class="p4"><span class="s1">MEDV<span class="Apple-converted-space"> </span></span></p>
      </td>
      <td valign="middle" class="td4">
        <p class="p4"><span class="s1">A numeric vector of median values of owner-occupied housing in USD 1000<span class="Apple-converted-space"> </span></span></p>
      </td>
    </tr>
    <tr>
      <td valign="middle" class="td3">
        <p class="p4"><span class="s1">CMEDV<span class="Apple-converted-space"> </span></span></p>
      </td>
      <td valign="middle" class="td4">
        <p class="p4"><span class="s1">A numeric vector of corrected median values of owner-occupied housing in USD 1000<span class="Apple-converted-space"> </span></span></p>
      </td>
    </tr>
    <tr>
      <td valign="middle" class="td3">
        <p class="p4"><span class="s1">CRIM<span class="Apple-converted-space"> </span></span></p>
      </td>
      <td valign="middle" class="td4">
        <p class="p4"><span class="s1">A numeric vector of per capita crime<span class="Apple-converted-space"> </span></span></p>
      </td>
    </tr>
    <tr>
      <td valign="middle" class="td3">
        <p class="p4"><span class="s1">ZN<span class="Apple-converted-space"> </span></span></p>
      </td>
      <td valign="middle" class="td4">
        <p class="p4"><span class="s1">A numeric vector of proportions of residential land zoned for lots over 25000 sq. ft per town (constant for all Boston tracts)<span class="Apple-converted-space"> </span></span></p>
      </td>
    </tr>
    <tr>
      <td valign="middle" class="td3">
        <p class="p4"><span class="s1">INDUS<span class="Apple-converted-space"> </span></span></p>
      </td>
      <td valign="middle" class="td4">
        <p class="p4"><span class="s1">A numeric vector of proportions of non-retail business acres per town (constant for all Boston tracts)<span class="Apple-converted-space"> </span></span></p>
      </td>
    </tr>
    <tr>
      <td valign="middle" class="td3">
        <p class="p4"><span class="s1">CHAS<span class="Apple-converted-space"> </span></span></p>
      </td>
      <td valign="middle" class="td4">
        <p class="p4"><span class="s1">A factor with levels 1 if tract borders Charles River; 0 otherwise<span class="Apple-converted-space"> </span></span></p>
      </td>
    </tr>
    <tr>
      <td valign="middle" class="td3">
        <p class="p4"><span class="s1">NOX<span class="Apple-converted-space"> </span></span></p>
      </td>
      <td valign="middle" class="td4">
        <p class="p4"><span class="s1">A numeric vector of nitric oxides concentration (parts per 10 million) per town</span></p>
      </td>
    </tr>
    <tr>
      <td valign="middle" class="td3">
        <p class="p4"><span class="s1">RM<span class="Apple-converted-space"> </span></span></p>
      </td>
      <td valign="middle" class="td4">
        <p class="p4"><span class="s1">A numeric vector of average numbers of rooms per dwelling</span></p>
      </td>
    </tr>
    <tr>
      <td valign="middle" class="td3">
        <p class="p4"><span class="s1">AGE<span class="Apple-converted-space"> </span></span></p>
      </td>
      <td valign="middle" class="td4">
        <p class="p4"><span class="s1">A numeric vector of proportions of owner-occupied units built prior to 1940<span class="Apple-converted-space"> </span></span></p>
      </td>
    </tr>
    <tr>
      <td valign="middle" class="td3">
        <p class="p4"><span class="s1">DIS</span></p>
      </td>
      <td valign="middle" class="td4">
        <p class="p4"><span class="s1">A numeric vector of weighted distances to five Boston employment centers<span class="Apple-converted-space"> </span></span></p>
      </td>
    </tr>
    <tr>
      <td valign="middle" class="td3">
        <p class="p4"><span class="s1">RAD<span class="Apple-converted-space"> </span></span></p>
      </td>
      <td valign="middle" class="td4">
        <p class="p4"><span class="s1">A numeric vector of an index of accessibility to radial highways per town (constant for all Boston tracts)</span></p>
      </td>
    </tr>
    <tr>
      <td valign="middle" class="td3">
        <p class="p4"><span class="s1">TAX</span></p>
      </td>
      <td valign="middle" class="td4">
        <p class="p4"><span class="s1">A numeric vector full-value property-tax rate per USD 10,000 per town (constant for all Boston tracts)</span></p>
      </td>
    </tr>
    <tr>
      <td valign="middle" class="td3">
        <p class="p4"><span class="s1">PTRATIO<span class="Apple-converted-space"> </span></span></p>
      </td>
      <td valign="middle" class="td4">
        <p class="p4"><span class="s1">A numeric vector of pupil-teacher ratios per town (constant for all Boston tracts)<span class="Apple-converted-space"> </span></span></p>
      </td>
    </tr>
    <tr>
      <td valign="middle" class="td3">
        <p class="p4"><span class="s1">B<span class="Apple-converted-space"> </span></span></p>
      </td>
      <td valign="middle" class="td4">
        <p class="p4"><span class="s1">A numeric vector of 1000*(Bk - 0.63)^2 where Bk is the proportion of blacks<span class="Apple-converted-space"> </span></span></p>
      </td>
    </tr>
    <tr>
      <td valign="middle" class="td3">
        <p class="p4"><span class="s1">LSTAT</span></p>
      </td>
      <td valign="middle" class="td4">
        <p class="p4"><span class="s1">A numeric vector of percentage values of lower status population</span></p>
      </td>
    </tr>
  </tbody>
</table>
</body>
</html>

## Baltimore Home Sales 1970s

### Dataset

<iframe src="https://drive.google.com/embeddedfolderview?id=1ea0Qm3dgYrq7LBAIUHXgTiG4R362Hb6_#grid" style="width:100%; height:600px; border:0;"></iframe>

### Description

<p>House sales price and characteristics for a spatial
   hedonic regression, Baltimore, MD 1978.</p>

<h2>Variables</h2>

<table>
<thead>
   <tr>
      <th>Variable</th>
      <th>Description</th>
   </tr>
</thead>
<tbody>
   <tr>
      <td>STATION</td>
      <td>ID variable</td>
   </tr>
   <tr>
      <td>PRICE</td>
      <td>sales price of house iin $1,000 (MLS)</td>
   </tr>
   <tr>
      <td>NROOM</td>
      <td>number of rooms</td>
   </tr>
   <tr>
      <td>DWELL</td>
      <td>1 if detached unit, 0 otherwise</td>
   </tr>
   <tr>
      <td>NBATH</td>
      <td>number of bathrooms</td>
   </tr>
   <tr>
      <td>PATIO</td>
      <td>1 if patio, 0 otherwise</td>
   </tr>
   <tr>
      <td>FIREPL</td>
      <td>1 if fireplace, 0 otherwise</td>
   </tr>
   <tr>
      <td>AC</td>
      <td>1 if air conditioning, 0 otherwise</td>
   </tr>
   <tr>
      <td>BMENT</td>
      <td>1 if basement, 0 otherwise</td>
   </tr>
   <tr>
      <td>NSTOR</td>
      <td>number of stories</td>
   </tr>
   <tr>
      <td>GAR</td>
      <td>number of car spaces in garage (0 = no garage)</td>
   </tr>
   <tr>
      <td>AGE</td>
      <td>age of dwelling in years</td>
   </tr>
   <tr>
      <td>CITCOU</td>
      <td>1 if dwelling is in Baltimore County, 0 otherwise</td>
   </tr>
   <tr>
      <td>LOTSZ</td>
      <td>lot size in hundreds of square feet</td>
   </tr>
   <tr>
      <td>SQFT</td>
      <td>interior living space in hundreds of square feet</td>
   </tr>
   <tr>
      <td>X</td>
      <td>x coordinate on the Maryland grid</td>
   </tr>
   <tr>
      <td>Y</td>
      <td>y coordinate on the Maryland grid</td>
   </tr>

</tbody>
</table>
</body>
</html>
