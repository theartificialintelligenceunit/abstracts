---
icon: lucide/rocket
---

# Background

The objective of this proof of concept is to investigate whether/how Amazon Web Services (AWS) tools can be used to develop data products or solutions that eliminate or minimise the organisation's manual operations/tasks.  <b>For example, products that</b>

<blockquote>
  Automatically <b>(a)</b> read data from one or more sources around the world, <b>(b)</b> inspect the data, address anomalies, and structure the data, <b>(c)</b> deliver structured data to defined points, <b>(d)</b> run sets of algorithms, e.g., business intelligence algorithms, on schedule, and <b>(e)</b> deliver a run's results to defined points.
</blockquote>

<b>And are</b>

<ul>
  <li>Secure.</li>
  <li>Developed within secure continuous integration, delivery, and deployment settings; this includes version control.</li>
  <li>In compliance with reproducibility and auditability mandates.</li>
  <li>Platform agnostic; subject to platform <b>(a)</b> interaction, and <b>(b)</b> programming interface constraints.</li>
</ul>

This concept illustrates AWS tools via hourly nitrogen dioxide readings, read by telemetric devices across Edinburgh.  The illustration is via two solutions<br><br>

<ol>
  <li>A <a href="https://github.com/excomputing/pollutants" target="_blank">one-off solution</a> that sets up a data depository within Amazon, and subsequently delivers historical Scottish Air Quality nitrogen dioxide data to the depository; after cleaning and structuring. </li>
  <li>A solution designed to operate daily.  Each day it automatically reads and structures the latest nitrogen readings, conducts quantiles and extrema calculations, and delivers the calculations to a point where a graph's data interface automatically reads it.</li>
</ol>

Instead of a graph, it could be a mobile app, an alert system, etc.

<br>
<br>

<br>
<br>

<br>
<br>

<br>
<br>
