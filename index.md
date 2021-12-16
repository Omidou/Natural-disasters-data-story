[Abstract](#abstract) <br>
[What data?](#what_data?) <br>
- [Filtered quotes](#filtered_quotes) <br>
[Natural disasters in the world](#natural_disasters_in_the_world) <br>
[Natural disasters in the US](#natural_disasters_in_the_us) <br>
[Analysis of speakers](#analysis_of_speakers) <br>
- [Topic detection](#topic_detection) <br>
[Conclusion](#conclusion)
  
<style>
p{
    text-align: justify;
}
</style>


## <a name="abstract"></a> Abstract 

<p>
Natural disasters, such as earthquakes, hurricanes, floods and wildfires, occur every year causing a lot of damage. Over the years, there has been a growing concern on the extent of climate change and on the potential impact it has on our current environment. The theories on the origin and on the nature of climate change have been flowing, there is still a lot of uncertainty on what to expect with it, but a shifting in the frequency and in the areas impacted by natural disasters has already been observed.
</p>
<p>
Every year, natural disasters impact the lives of thousands of people across the world, and as the main cause of many disruptions in the world, it is fair to expect the impact of these unfortunate events to spread to the media and the press. This story aims to depict how quotations taken from the news are able to reflect the natural events that have taken place and impacted the real world, and in a reverse manner, how the impact of natural disasters can be observed in the media. <br>
</p>

## <a name="what_data?"></a> What data?

<p>
The QuoteBank dataset consists of millions of quotations found in online articles. Our analyses will be based on using these numerous quotes as an indicator of the overall media coverage of an event, thanks to their large number and to their diversity. It is possible to extract quotes relevant to the subject of natural disasters by selecting the ones citing specific words from a curated dictionary of diverse catastrophes. Along with the help of two datasets containing ground truth information on different kind of natural disasters <a href="https://www.emdat.be/">worldwide</a>, and most specifically <a href="https://www.kaggle.com/headsortails/us-natural-disaster-declarations">in the US</a>, we can try to see what parallels can be drawn between real data about natural disasters and quotes related to them. <br>
</p>
<p>
The quotes being in English, most of the quotations are most likely to be driven towards US-related material and events or towards events that have made such an impact that it is worth mentioning in the english or american news. The US natural disaster dataset allows us to have a more precise idea of where specifically in the US the unfortunate events took place, as it encodes county-wise information about the disasters. <br>
</p>

### <a name="filtered_quotes"></a> Filtered quotes

<p>
To specifically target quotes that are relevant to the subject of natural disasters, only the quotes containing words part of a list of words relevant to the subject are kept, such as 'hurricane', 'earthquake', 'fire', and so on. The time distribution of the filtered quotes is shown below :
</p>

<p style="text-align: center"><img src="figures/overall_quote_distribution.png" /><br>Distribution of the filtered quotes over time</p>

<p>
The filtered quotes make up for a total of around 1500000 quotes, leaving us with a high number of quotes to work with. The frequency of the quotes is overall uniform despite a few drops, meaning that we can draw consistent comparisons if we compare the frequency of occurence of certain types of quotes in different period of times.
</p>

<p>
On the other hand, the separate distributions in time of each natural disaster of interest show very irregular and spiky shapes for most of them (figure below). These spikes in frequency mean that there are short periods of time which resulted in a use of the disaster name in the quotes that is far higher than usual. These already suggest that there was increased attention driven towards each natural disaster, already encoding some temporal information about the occurence of each natural disaster in the world or in the United States.
</p>

<p style="text-align: center"><img src="figures/nd_quote_distribution.png" /><br>Specific distribution of the quotes over time for each natural disaster type of interest</p>

## <a name="natural_disasters_in_the_world"></a> Natural disasters in the world

<p>
First getting an insight of how natural disasters affect the world in various ways depending on the area can help us with understanding what quotes to target in order to extract interesting facts from them. Feel free to slide between the different distributions of natural disasters in the world to get a better idea of the pattern with which these unfortunate events strike different areas of the world. The darker the country, the more times it has been struck by an event of the type defined by the slider. Note that data on the natural disasters occuring in countries such as the US are more likely to be reported due to the stronger influence of the american media on an international level as compared to other, smaller countries. This explains why the US are displayed as heavily impacted by most of those disasters and justifies why later focus on the US natural disaster dataset makes sense. 
</p>

<div style="width: 100%; height: 80vh; text-align: center; vertical-align: middle;"><iframe src="figures/slider_disasters.html" style="width: 100%; height: 100%; background-color: transparent; border: 0px none transparent; padding: 0px;"></iframe>Distribution of reported natural disasters per type</div><br>

<p>
Looking at the earthquake distribution across the globe, we see that there seems to be an area that is particularly prone to experiencing earthquakes. If we zoom in, we see that the whole area including China, Iran, Indonesia and the Philippines has been subject to many earthquakes in recent times. <br>
</p>
<p>
ZOOMED IN PICTURE <br>
</p>

<img src="figures/earthquake_scheme.png" />



<!---
TO ADD THE INTERACTIVE PLOT
-->
<div style="width: 100%; height: 80vh; text-align: center; vertical-align: middle;"><iframe src="figures/left_map.html" style="width: 100%; height: 100%; text-align: center; background-color: transparent; border: 0px none transparent; padding: 0px;"></iframe>Map of the number of hurricanes across the US</div><br>


<!---
<p>Map Test 18</p>

<iframe width="1250px" height="860px" src="figures/lda_res_pol.html" style="-webkit-transform:scale(0.65);-moz-transform-scale(0.65); position: absolute; top: -9999px; bottom: -9999px; left: -9999px; right: -9999px; margin: auto;"></iframe>

<style>
.iframe-container {
  overflow: hidden;
  /* 16:9 aspect ratio */
  padding-top: 56.25%;
  position: relative;
}

.iframe-container iframe {
   border: 0;
   height: 100%;
   left: 0;
   position: absolute;
   top: 0;
   width: 100%;
   -webkit-transform: scale(0.7);
   -moz-transform: scale(0.7);
}
</style>
  
<div class="iframe-container">
  <iframe src="figures/lda_res_pol.html" allowfullscreen></iframe>
</div>
  
  
<p>
  NEW TEST 6
</p>

<style>
.wrap {
  width: 640px;
  height: 480px;
  overflow: hidden;
}

.wrap iframe {
  width: 142.85% !important;
  height: 142.85% !important;
  -webkit-transform: scale(0.7);
  transform: scale(0.7);
  -webkit-transform-origin: 0 0;
  transform-origin: 0 0;
}
</style>

<div class='wrap'>
    <iframe src="figures/lda_res_pol.html"></iframe>
</div>


<div style="width: 100vw; height: 100vh; text-align: center"><iframe style="width: 100%; height: 100%; -webkit-transform: scale(0.7); -moz-transform: scale(0.7);" src="figures/lda_res_pol.html" ></iframe>Topic detection of quotes where the speaker is a politician or a researcher</div>
-->
<!---
<div style="width: 100vw; height: 100vh; text-align: center"><iframe style="width: 100%; height: 100%; -webkit-transform: scale(0.6); -moz-transform: scale(0.6); -webkit-transform-origin: top left;" src="figures/lda_res_pol.html" ></iframe>Topic detection of quotes where the speaker is a politician or a researcher</div>
-->

#### Exploration

With a quick look at the frequency of natural disasters key words in the quotations, one can observe peaks that most likely indicate the crisis. <br/>

<div style="text-align: center;">
  <img src="https://user-images.githubusercontent.com/43467181/145828341-c93ade7f-1cfd-401d-8849-c8c51b9c1da2.png" width="450" />
  <img src="https://user-images.githubusercontent.com/43467181/145828332-d9097924-8e90-440b-a532-539ca9ce9f7c.png"  width="450" /> 
</div>

These can be easily verified with the ground truth dataset. <br/>
Note that with some inspection, one can notice that some quotes contain natural disaster key words, but in other contexts like comparisons or hyperboles (E.g. Fire, storm, earthquake, ...). Here is another example for Wildfires cases. <br/>

<div style="text-align: center;">
  <img src="https://user-images.githubusercontent.com/43467181/145827748-b9c84c5a-4a11-4598-b219-a6ccaa331aee.png" />
</div>

Furthermore, the location of the disaster can also be found in those quotes either by looking for states or cities inside the quotations or by comparing the dates of the frequency peaks with the ground truth dataset of natural crises and extracting the location. Here is an example for hurricanes. <br/>

<div style="text-align: center;">
  <img src="https://user-images.githubusercontent.com/43467181/145830940-40e02dd2-6204-4079-ac4a-7693afefef70.png" />
</div>

Unsurprisingly, quotes that talk about hurricanes also frequently mention Florida and Texas. <br/>
Hence there is enough data to start constructing a spatial and temporal map of natural disasters. <br/>

## <a name="analysis_of_speakers"></a> Analysis of speakers

<p>
Now, let us investigate the speakers. What are their professions? For the politicians, what are their political affiliations? In the following graph we have plotted the distribution of the ten most common professions among the speakers in our list. Since we suspected that politicians may speak much more often than other groups we also plotted the distribution of quotes per profession.
</p>

<img src="figures/occupation.png"/>
<img src="figures/num_quotes_by_occupation.png"/>

<p>
We see that among the top ten groups, politicians speak slightly more often, but this increase is small enough that we can pretend that every unique speaker gives approximately the same number of quotes.
We see that the most frequent speakers are researchers followed by politicians. The rest of the occupations trail behind, having roughly the same frequency each.
</p>

<!-- TODO Maybe remove this bit -->
<p>
In the following graph we have plotted the distribution of the ten most common political affiliations among our speakers.
</p>

<img src="figures/parties.png"/>

<p>
The parties that appear most often are those that operate in english-speaking countries. This is unsurprising given that we work with english quotes.
</p>



[Later in the article](#### Researcher vs Politicians: How does the way they speak differ ?), we will perform a bag-of-words logistic regression to differentiate researcher quotes with politician quotes.
Having found a good fit, in [the section after it](#### Topic Detection) we will display the result of a latent Dirichlet analysis (LDA), in the hopes of detecting what are the two main topics each group is talking about.

## Results
(--- move methods here ?)


### <a name="logistic_regression"></a> Researcher vs Politicians: How does the way they speak differ ?
TODO

### <a name="topic_detection"></a> Topic Detection
<a href="figures/lda_res_pol.html">*See the LDA on a standalone page*</a>
<div style="width: 100%; height: 80vh; text-align: center"><iframe src="figures/lda_res_pol.html" style="width: 100%; height: 100%; object-fit: contain; text-align: center; background-color: transparent; border: 0px none transparent; padding: 0px; margin-left: 0px" frameborder='0' ></iframe>Topic detection of quotes where the speaker is a politician or a researcher</div><br>


<br><br>


## <a name="conclusion">Conclusion</a>
blabla


