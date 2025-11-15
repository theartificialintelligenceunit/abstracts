---
icon: lucide/circle-question-mark
---

# Background

## Aim

In brief.  Organisations identify or detect words/strings of interest within documents or data blobs for a variety of purposes, e.g., knowledge graph development, text redaction, criminal investigations, etc.  Organisations may opt for manual word detection if off-the-shelf solutions cannot address their needs.  For example, most redaction software solutions focus on detecting and redacting words/strings of a narrow set of categories, and it is rarely possible to adapt the solution to the detection of words/strings of bespoke categories.

<br>

A viable solution strategy involves the creation of custom models via <i>named entity recognition</i> machine learning algorithms; also known as token classification algorithms. These algorithms can be trained by domain or problem, leading to compact, domain specific, word/string detection models.

<br>

This project publishes an adaptable token classification modelling set-up, i.e., artificial/machine learning engineers can fork and adapt the repositories to their $(a)$ token classification problem, $(b)$ development environment, and $(c)$ the <a href="https://github.com/membranes/text/blob/master/src/models/interface.py#L70">range of language models</a> that they would like to try.  The latter point is discussed below.

<br>
<br>

## Assets

The [membranes hub](https://github.com/membranes) hosts the repositories of a token classification modelling project.  Readers may interact with the model via a [simple open interface](https://greyhypotheses-detecting.hf.space).

<br>

### Repositories

The diagram outlines the functions of git repositories; hover over a git symbol for a brief summary of a repository's function.

<br>

<img src='../../../images/dispatches-repositories.png' alt='repositories' width='685'/>

<br>

The `text` package will be re-written, if funding is available.  The
<a href="https://github.com/membranes/restructuring" target="_blank">restructuring</a> repository package is for restructuring the latest data captures in preparation for (a) human inspection, and (b) usage as a model re-training data source.

<br>

### Model & Data

* [Model Description]()
* [Data Description]()

<br>
<br>

## Application

This section outlines a plausible $(a)$ problem statement, $(b)$ corresponding outcome expectations/underlying aims, and $(c)$ deployment goal vis-à-vis token classification model development.

<br>

### Problem Statement

An organisation manually classifies trauma incidents for all the major trauma centres of five countries.  Per trauma case, an injury coding expert <b>(a)</b> examines the case's free and structured text, and assigns each piece of text to a category, and <b>(b)</b> assigns the case to a trauma category based on the combination text pieces & categories detected; text pieces of the other/miscellaneous category are excluded from this exercise.  Trauma injury coding is an extremely intensive and time-consuming exercise, and injury coding error rates - per annum - can be quite high.  Hence, and as a first step, we are in search of a solution that automatically classifies text pieces vis-à-vis a set of provided categories.

<br>

### Outcome Expectations, Underlying Aims

- <b>Outcome Expectations:</b> Real-time availability of classifications per trauma case.
- <b>Underlying Aim:</b> The automatic classification of trauma case text pieces; objective &#8594;

    * per case, automatic classification time < 180 seconds.
    * model metrics limits false negative rate &#8804; 0.02, false positive rate &#8804; 0.04

<br>

### Deployment Goal

A potential machine learning dependent project without a deployment goal is directionless, do not proceed.  A plausible deployment goal is<br><br><br><br>

<img src='../../../images/dispatches-deployment-goal.png' alt='deployment goal' width='596'/>

<br>
<br>

<br>
<br>

<br>
<br>

<br>
<br>
