---
icon: lucide/workflow
---

# Orchestration & Automation

An outline of the concept product.

## Architecture

The illustration below outlines the proof of concept architecture; <b>enlarge the illustration via the </b><i>fit</i> <b>or</b> <i>zoom</i><b> buttons, at the bottom of the illustration</b>.  <b>For more details about an item/icon, hover over the item/icon; a few icons have links to more details.</b>  Assets, e.g., container images, are delivered to Amazon Web Services (AWS) via GitHub.<br><br>


<p style="margin-left: 35px;">LAUNCH DIAGRAM</p>


The GitHub Organization <a href="https://github.com/excomputing"><i>excomputing</i></a> hosts all the repositories of this project.  In line with the <b>agnostic solutions</b> request, all computations are via containers.  Container image registration is automatic, it occurs during pushes to GitHub, i.e., it is part of this project's continuous integration, delivery, & deployment set-up; the registries are

<ul>
  <li><a href="https://docs.aws.amazon.com/AmazonECR/latest/userguide/what-is-ecr.html" target="_blank">Amazon Elastic Container Registry</a></li>
  <li><a href="https://docs.github.com/en/packages/working-with-a-github-packages-registry/working-with-the-container-registry#about-the-container-registry" target="_blank">GitHub Container Registry</a>.</li>
</ul>

A GitHub Actions event <b>(a)</b> builds an image of a repository, and <b>(b)</b> delivers the image to either or both registries; these steps automatically occur during on-master-push to GitHub.<br><br>

<br>
<br>

<br>
<br>

<br>
<br>

<br>
<br>
