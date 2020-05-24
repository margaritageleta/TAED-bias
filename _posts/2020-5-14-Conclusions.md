---
layout: post
title: "Conclusions"
description: "In this section we explain the conclusions we extracted from the activities we had organized in the Algorithmic Research Session. "
permalink: /phase5/
image: img/pattern1.jpg
---

### Quiz:

We have asked students to translate some words into Catalan/Spanish from English in order to see what gender pronoun they use in the translation, this way we can detect gender biases:

<div style="width: 100%; height:200px; display:flex; justify-content: center; align-items: center; margin-top: 15px; margin-bottom: 15px;">  
      <div style="background-image: url('../img/conclusions/1.png'); height:100%; width:80%; background-repeat: no-repeat; background-size: contain; background-position:center;"></div>
</div>

The differences in gender based on occupation are a reflection of the reality. If data is not treated to reduce these differences, the model could inherit unfair discrimination present in our society. Therefore, it could produce recurrent negative feedback and enhance the differences.

Then we propose some phrases and we ask about what is the first they think:

<div style="width: 100%; height:200px; display:flex; justify-content: center; align-items: center; margin-top: 15px; margin-bottom: 15px;">  
      <div style="background-image: url('../img/conclusions/2.png'); height:100%; width:80%; background-repeat: no-repeat; background-size: contain; background-position:center;"></div>
</div>

Everyone sees the world through their own biases. We have to be careful not to impose the bias of the majority to minorities.

Finally, bias can be found in 3 phases: in training data, in the algorithm itself and in validation. We have asked students, what is mode critical to deal with when trying to solve the bias issue:

<div style="width: 100%; height:200px; display:flex; justify-content: center; align-items: center; margin-top: 15px; margin-bottom: 15px;">  
      <div style="background-image: url('../img/conclusions/3.png'); height:100%; width:80%; background-repeat: no-repeat; background-size: contain; background-position:center;"></div>
</div>

### Activity 1: DEBATE algorithmic bias examples
4 interesting and contradictory situations about bias in the algorithms were be discussed. Students have discussed both points of view and some conclusions have been drawn.

#### Instagram hashtags
Certain hashtags are not allowed in Instagram due to the amount of times they have been reported. Two points of view:
- This is OK. If a hashtag is reported many times, it is often due to its content being not appropriate.
- It is a matter of checking that discriminatory behaviour when reporting publications does not imply blocking of discriminated minorities’ publications.

#### Google Photos
In Google Photos’ search algorithm, photos containing black people pop up when searching for “gorilla”. Two points of view:
- Modifications should be applied to the model in order to avoid racist classifications.
- It is not a racist classification, but the algorithm simply observes physical similarities (i.e., the colour of the skin) and so it fails in some cases.

#### Employment website
It has been discovered that in some employment websites, the jobs offering better pay are shown mostly to men. Two points of view:
- The algorithm is inheriting the bias in society thus hindering the equality among men and women in terms of workplace.
- The algorithm must recommend jobs which are more suitable to the user. If it observes features of the user indicating the preference of a job over another, why should it show another?

#### Intelligent surveillance systems
Surveillance cameras detect women and Asian men committing crimes poorly, while they do so well for young men.
- If there are more young men committing crimes, it is fine that the algorithm focuses on identifying this group properly.
- The database should be modified in order to debias the algorithm and make it detect all criminals equally, even if this implies performance losses in some groups.

### Activity 2: DEBATE on some of the Datasheet Questions
Several questions were asked about the News v15 dataset:
- Do you think included languages are equally represented in the corpora?
Students have discussed quantitative and qualitative differences, and have noticed that there is not the same amount of historic records for every language.
- Is there any evidence that the data shows any kind of bias?
Everybody agreed that the dataset consisted of articles on economics and politics.
- Vocabulary enrichment is done automatically, do you think this can introduce more bias?
The answer to this question has been summarized in: "Trash in, Trash out".
- Does it make sense to neutralize the bias present in the data given the bias inherent in society?
It was a open question, students coincided in that we should fight against the existing social bias. However, it will be hard.

Finally, students had to imagine that they were workers in the Data Science departament of a newspaper. The task was to create a Machine Translation tool that allows to read the news in all languages (for the next election). Students discussed two seetings:
- **Situation 1**: a political party offers you a dataset created by them.
- **Situation 2**: your work team has managed to find a dataset but it is biased.

### TAKE-HOME WORK
In the take-home activity, students were asked to say which of the Datasheets points they think are the more insightful with respect to data. Just a reminder: remember that the Datsheets sections include: (1) Motivation, (2) Composition, (3) Collection Process, (4) Preprocessing, (5) Uses, (6) Distribution Process, (7) Maintenance.

Below we show the results of the poll - 50% of the students showed to believe that the Collection Process is the most informative part regarding data.

<div style="width: 100%; height:200px; display:flex; justify-content: center; align-items: center; margin-top: 15px; margin-bottom: 15px;">  
      <div style="background-image: url('../img/conclusions/4.png'); height:100%; width:80%; background-repeat: no-repeat; background-size: contain; background-position:center;"></div>
</div>

Next, we asked students to propose key aspects for each of the above sections. What would be of maximum relevance to know regarding data if we had no available Datasheets? In the following sections we expose interesting points that Data Science students have found out.

#### Key aspects to Motivation

- **The creator of the dataset**: good reputation leads to confidence and reliability of the dataset.
- **The purpose of the dataset**: to the know Why? we can also discover some biases by knowing the original aim of the dataset.

#### Key aspects to Composition

- **The confidentiality of the data**: is the data protected? Does it include non-public content about certain individuals? We cannot break the law.
- **The dataset record**: a record of all the modifications and transformations of the dataset.

#### Key aspects to Collection Process

- **The origin**: where does the data come from?
- **The way it was collected**: (a) Was there consent to collect this kind of data? (b) Is it reliable and trustworthy?

#### Key aspects to Preprocessing

- **Outliers & Missing values**: depending on the preprocessing done, this step can induce bias …
- **Debiasing techniques**: has there been bias removal during the preprocessing stage? Describe the details needed / known.
- **Anonymization techniques**: it is key to respect the GDPR.
- **Feature neglection**: why some features are ignored or deleted?

#### Key aspects to Uses

- **Intended tasks**: in which tasks can this dataset be used?
- **Actual tasks**: examples of use. Who used it?
- **Licences**: are there any restrictions in use?

#### Key aspects to Distribution Process

- **Licenses, again**: who will be in control of the data? Under which regulation will be the dataset distributed? What kind of intellectual property laws reign over it?
- **Distribution channels**: how is this dataset distributed?
- **Accessibility**: is it private / public? Is it difficult to have access to the data?

#### Key aspects to Maintenance

- **Last update**: data evolves in time!
- **Update periodicity**: will it be updated when it will be needed?
- **The way it is updated**: avoid manipulation and bias.
- **The responsible**: contact & transparency.
- **Contributions**: who can contribute?

<div style="width: 100%; height:200px; display:flex; justify-content: center; align-items: center; margin-top: 15px; margin-bottom: 15px;">  
    <a href="https://margaritageleta.github.io/TAED-bias/">
        <div style="background-color: teal; height:65px; width:175px;display: flex; justify-content: center; align-items: center; border-radius: 7px;">
            <p style="margin: 0; color: white;">HOME</p>
        </div>
    </a>
</div>
