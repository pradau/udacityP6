README.md
September 16, 2016
This html file is my first project to create an animated graphic from dimple, D3 and 
javascript.

### Summary:
Batting results might be thought to be directly related to player size.
In this graph the summed Home Runs (HRs) are plotted as a function of Body Mass Index,
where BMI=mass(kg)/height(m)^2. BMI is often used as a measure of a person's size,
and in a fit individual it generally increases with strength (rather than obesity).
The graph also shows handedness as bar color.
Chart 1:
The graph demonstrates that there are more HRs from right-handers (RHs) than left-handers 
(LHs) or both-handers (BHs), for each of the BMI categories. Likewise the HRs from LHs are 
greater than HRs from BHs in each BMI category. However, the effect of BMI size on HRs is 
unclear because the number of players in each handedness category is not fixed. The 
second graph is intended to address this issue.
Chart 2:
For this graph, the HRs are normalized to the same number of players (1000) per handedness 
category. This graph clarifies that there is a lower rate of HRs from the small (BMI <=23) 
players than either the medium or large players. The LH players have a higher rate of HRs 
than the two other handedness categories (for medium and large players). The RH players 
have a trend of higher HRs depending on player size (largest players have the highest HRs; 
smallest players have the lowest HRs). This trend is not present with the BH players.

### Design:
The charts are bar charts indicating Home Runs for each player size category. The colors 
(and legend) indicate the handedness. The legend interaction allows the viewer to examine 
and compare two player sizes for a given handedness. The BMI (calculated in Excel from 
height and weight) was chosen as the independent axis because neither height or weight are 
not as helpful to indicate the player build, as was confirmed by exploratory graphing.
This was further refined to 3 categories (BMI-Type) to aggregate players of similar size.
Batting average was not used because it did not appear to be predictive of HRs.

### Feedback:
Remarks on the previous version of the chart.
Feedback 1:
I recommend not using a stacked bar chart, and instead a regular bar chart.
A stacked bar chart is misleading about the absolute number of HRs. For example there are 
many fewer HRs in the small player category, therefore a stacked bar chart for each size 
category would give a false impression that small players contribute many HRs compared to 
other player sizes.

Feedback 2:
You should collect the results by BMI categories (small, medium, large). Otherwise it is 
difficult to discern a trend with player size.

Feedback 3:
Try normalizing the data so that there is an equivalent number of people in each 
handedness category. Otherwise any size trend is confused by the much higher number of
right-handed players.

### Reflection:
I think it was important to try several different graphs in order to get a sense of what 
idea I might want to convey in the final graph. The idea of presenting some relationship 
between the player size and the batting results was suggested by the available data but it 
wasn’t clear which to use. Some initial graphing also suggested what “cleanup” was needed 
(e.g. for zero BA values and for duplicate names).  The Udacity reviewer rightly pointed 
out that overplotting in my first submission made the bubble chart difficult 
to interpret. Therefore I can see that trying more chart types (e.g. histograms, bar 
charts) are important before deciding on the final visualization.

### Resources:
Body Mass Index
https://en.wikipedia.org/wiki/Body_mass_index

Dimple
http://dimplejs.org/

Stackoverflow
Various Q&A on dimple e.g.
http://stackoverflow.com/questions/22991143/dimple-js-values-in-bar-chart-outside-chart