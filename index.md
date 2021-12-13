1. [Introduction](#introduction)
  - [Abstract](#abstract)
  - [What data?](#what_data?)
  - [Methods](#methods)

2. [Results](#results)
  - [Map of natural disasters](#map_of_natural_disasters)
  - [Analysis of speakers](#analysis_of_speakers)
3. [Conclusion](#conclusion)
4. [References](#references)


## Introduction

Test TITLE

<!---
TO ADD THE INTERACTIVE PLOT
-->
<div style="width: 100%; height: 80vh; text-align: center"><iframe src="left_map.html" style="width: 100%; height: 100%; text-align: center; background-color: transparent; border: 0px none transparent; padding: 0px;"></iframe>Map of the number of hurricanes across the US<br></div>

<!---
margin-left: auto; margin-right: auto;
-->

### Abstract 
More complete abstract than the one in the readme + research questions updated <br/>
TODO AT THE END


### <a name="what_data?"></a> What data?

The QuoteBank dataset consists of quotations found in online articles. With the help of a dataset containing ground truth informations on different kind of natural disasters [worldwide](https://www.emdat.be/), and most specifically [in the US](https://www.kaggle.com/headsortails/us-natural-disaster-declarations), it is possible to extract quotes by manually taking the ones citing specific words from a curated dictionary of diverse catastrophes. <br/>

#### Exploration

With a quick look at the frequency of natural disasters key words in the quotations, one can observe peaks that most likely indicate the crisis. <br/>

<p align="center">
  <img src="https://user-images.githubusercontent.com/43467181/145828341-c93ade7f-1cfd-401d-8849-c8c51b9c1da2.png" width="450" />
  <img src="https://user-images.githubusercontent.com/43467181/145828332-d9097924-8e90-440b-a532-539ca9ce9f7c.png"  width="450" /> 
</p>

These can be easily verified with the ground truth dataset. <br/>
Note that with some inspection, one can notice that some quotes contain natural disaster key words, but in other contexts like comparisons or hyperbole (E.g. Fire, storm, earthquake, ...). Here is another example for Wildfires cases. <br/>

<p align="center">
  <img src="https://user-images.githubusercontent.com/43467181/145827748-b9c84c5a-4a11-4598-b219-a6ccaa331aee.png" />
</p>

Furthermore, the location of the disaster can also be found in those quotes either by looking for states or cities inside the quotations or by comparing the dates of the frequency peaks with the ground truth dataset of natural crises and extracting the location. Here is an example for hurricanes. <br/>

<p align="center">
  <img src="https://user-images.githubusercontent.com/43467181/145830940-40e02dd2-6204-4079-ac4a-7693afefef70.png" />
</p>

Unsurprisingly, quotes that talk about hurricanes also frequently mention Florida and Texas. <br/>
Hence there is enough data to start constructing a spatial and temporal map of natural disasters. <br/>


MAYBE ADD SOMETHING FOR SPEAKERS?

### Methods
Quick summary of what was done for maps + analysis of speakers (? maybe not necessary)

## Results
(--- move methods here ?)

### <a name="map_of_natural_disasters"></a> Map of natural disasters
Map + explanation 

### <a name="analysis_of_speakers"></a> Analysis of speakers
TODO

## Conclusion
blabla

### References

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [Basic writing and formatting syntax](https://docs.github.com/en/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax).
