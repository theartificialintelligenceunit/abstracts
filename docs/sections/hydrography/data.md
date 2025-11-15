---
icon: lucide/grip
---

# Data

## Sources

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

## Weather Warnings & Meteorological Office

[Meteorological Office Warnings Services](https://weather.metoffice.gov.uk/guides/warnings):

* [RSS feeds](https://weather.metoffice.gov.uk/guides/rss)
* [email alerts](https://www.metoffice.gov.uk/about-us/news-and-media/media-centre/subscribe-to-email-alerts)
* [National Severe Weather Warnings Service Public API](https://metoffice.github.io/nswws-public-api)

<br>
<br>

<br>
<br>

<br>
<br>

<br>
<br>
