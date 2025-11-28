---
icon: lucide/circle-question-mark
---

# Background

## About

The objective of this exercise is to illustrate how Amazon Web Services (AWS) tools enable the <a href="https://www.ibm.com/think/topics/automation-vs-orchestration" target="_blank">orchestration & automation</a> of end-to-end solutions that eliminate or minimise the manual steps of - data dependent - operations, tasks.  <b>For example</b>

!!! note "A solution that can"
    
    Automatically <b>(a)</b> read data from one or more sources around the world, <b>(b)</b> inspect the data, address anomalies, and structure the data, <b>(c)</b> deliver structured data to defined points, <b>(d)</b> run sets of algorithms, e.g., business intelligence algorithms, on schedule, and <b>(e)</b> deliver a run's results to defined points.


!!! note "and is"
    
    <ul>
      <li>Secure.</li>
      <li>Developed within secure continuous integration, delivery, and deployment settings; this includes version control.</li>
      <li>In compliance with reproducibility and auditability mandates.</li>
      <li>Platform agnostic; subject to platform <b>(a)</b> interaction, and <b>(b)</b> programming interface constraints.</li>
    </ul>


## Illustration

To illustrate <a href="https://www.ibm.com/think/topics/automation-vs-orchestration" target="_blank">orchestration & automation</a> via AWS tools, the exercise focuses on providing daily quantile distributions of nitrogen dioxide levels within a city.  The city in focus is Edinburgh, which has a few telemetric measuring devices across the city.

The solution has two parts<br>

<ol>
  <li>A <a href="https://github.com/excomputing/pollutants" target="_blank">one-off solution</a> that sets up a data depository within Amazon, and subsequently delivers historical Scottish Air Quality nitrogen dioxide data to the depository; after inspecting and structuring. </li>
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
