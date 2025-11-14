---
icon: lucide/rocket
---

# Data & Algorithms

## Data

### Sources

The data sources:

<table style="width: 85%; margin-left: 35px; vertical-align: top;">
  <colgroup>
      <col span="1" style="width: 18.5%;">
      <col span="1" style="width: 43.5%;">
  </colgroup>
  <thead><tr style="text-align: left"><th>&nbsp;</th><th>Notes</th></tr></thead>
  <tr><td><abbr title="Scottish Environment Protection Agency">SEPA</abbr> Hydrometric Data</td>
      <td><a href="https://timeseriesdoc.sepa.org.uk" target="_blank"><abbr title="Scottish Environment Protection Agency">SEPA</abbr> API</a> &rarr;<br><a href="https://timeseriesdoc.sepa.org.uk/api-documentation/" target="_blank">application programming interface documentation</a>, <a href="https://timeseries.sepa.org.uk/KiWIS/KiWIS?datasource=0&service=kisters&type=queryServices&request=getrequestinfo" target="_blank">query service</a>, water levels [<a href="https://www.sepa.org.uk/environment/water/water-levels/">1</a>, <a href="https://waterlevels.sepa.org.uk/">2</a>], <a href="https://timeseriesdoc.sepa.org.uk/api-documentation/before-you-start/what-controls-there-are-on-access/">access controls</a>, <a href="https://timeseriesdoc.sepa.org.uk/api-documentation/before-you-start/how-data-validity-may-change/">river level data quality codes</a>, <a href="https://www.sepa.org.uk/environment/environmental-data/"><abbr title="Scottish Environment Protection Agency">SEPA</abbr> Environmental Data</a>, <a href="https://www.gov.uk/government/publications/uk-geospatial-data-standards-register/national-geospatial-data-standards-register">geospatial standards register</a>, <a href="https://waterdata.usgs.gov/blog/gage_height/">gauge height</a>, <a href="https://www.usgs.gov/media/images/gage-datum-reference-point">gauge datum reference point</a></td></tr>
  <tr>
    <td>Granular Catchment Polygons</td>
    <td><abbr title="Centre for Environment Fisheries and Aquaculture Science">CEFAS</abbr>: <ul><li>Catchment Boundaries Pages &Rarr; <a href="https://data.cefas.co.uk/view/21969" target="_blank">1</a>, <a href="https://data.cefas.co.uk/view/21970" target="_blank">2</a></li><li><a href="https://www.cefas.co.uk/data-and-publications/cefas-data-hub-apis">Application Programming Interface Details</a></li></ul></td>
  </tr>
  <tr><td>Care Homes</td><td>A raw <a href="https://data.spatialhub.scot/dataset/care_homes_for_older_people-is" target="_blank">gazetteer of Scotland's care homes</a> is available via <a href="https://data.spatialhub.scot/dataset/care_homes_for_older_people-is">Scotland's Spatial Hub</a>. For programmatic retrieval
  <pre>
    <b>{file.name}</b> = Care_Homes_for_Older_People_-_Scotland
    url = 
      &quot;https://geo.spatialhub.scot/geoserver/sh_chep/wfs
        ?service=WFS
          &authkey=<b>{authentication.key}</b>
            &request=GetFeature
              &typeName=sh_chep:pub_chep
                &format_options=filename:<b>{file.name}</b>
                  &outputFormat=application/json&quot;
  </pre></td>
  </tr>
</table>

<br>

### Weather Warnings & Meteorological Office

[Meteorological Office Warnings Services](https://weather.metoffice.gov.uk/guides/warnings):

* [RSS feeds](https://weather.metoffice.gov.uk/guides/rss)
* [email alerts](https://www.metoffice.gov.uk/about-us/news-and-media/media-centre/subscribe-to-email-alerts)
* [National Severe Weather Warnings Service Public API](https://metoffice.github.io/nswws-public-api)

<br>
<br>

## Risks

This page outlines tools under investigation for real-time *areas at risk* identification.

### Rates of Change of River Level

Let

$$\mathcal{l}_{t}, \: \mathcal{l}_{t - \tau}, \: \mathcal{l}_{t - 2\tau}, \: \mathcal{l}_{t - 3\tau}, \: \ldots$$


represent the time series of a gauge's river level measures, separated by $\tau$ hours, and unit of measure &Rarr; millimetres. Then the weighted-rate-of-change, w.r.t. each $\tau$ hours interval, is


$$r_{t - i\tau} = \frac{1}{\tau} \bigl(\mathcal{l}_{t - i\tau} - \mathcal{l}_{t - (i + 1)\tau}\bigr) \times \frac{1}{\mathcal{l}_{t - (i + 1)\tau}} \bigl(\mathcal{l}_{t - i\tau} - \mathcal{l}_{t - (i + 1)\tau}\bigr) $$

wherein

* $i = 0, 1, 2, 3, \ldots$
* $t\:$ is a/the current time point.
* $r_{t - i\tau}\:$ is the rate of change at time point $t - i\tau$, and its unit of measure is millimetres/hour.

Noting that

$$\frac{1}{\mathcal{l}_{t - (i + 1)\tau}} \bigl(\mathcal{l}_{t - i\tau} - \mathcal{l}_{t - (i + 1)\tau}\bigr)$$

determines the relative river level change w.r.t. consecutive river level values, i.e., values that are $\tau$ hours apart.


<br>
<br>

## Drift

For time series drift calculations, this hub depends on

* Jensen-Shannon Distance $J_{dist}$
* Wasserstein Distance $\mathcal{W}$

<br>wherein

$$J_{dist} = \sqrt{J_{div}}$$

$J_{div}$ is the Jensen-Shannon Divergence, a method for determining the similarity of a pair of distributions[^jensen].  The similarity between a pair of distributions increases as $J_{dist} \rightarrow 0$.  Note, for a pair of distributions

$$J_{div} \in [0 \quad 1]$$

therefore

$$J_{dist} \in [0 \quad 1]$$

The Wasserstein Distance <b>is</b> a distance measure[^wasserstein].

Important, do not consider scores in isolation, also consider the pattern of the scores over time.

<br>
<br>

<br>
<br>

<br>
<br>

<br>
<br>

[^jensen]: Study <a href="https://ieeexplore.ieee.org/document/61115" target="_blank">Divergence Measures Based on Shannon Entropy</a> for an in-depth understanding of Jensen-Shannon Divergence.
[^wasserstein]: Part 6 of <a href="https://arxiv.org/pdf/1904.08994" target="_blank">From GAN to WGAN</a> has an in-depth discussion of the Wasserstein Distance.  <span style="color: #a3a0a0">GAN: Generative Adversarial Network, WGAN: Wasserstein Generative Adversarial Network</span>

<br>
<br>
