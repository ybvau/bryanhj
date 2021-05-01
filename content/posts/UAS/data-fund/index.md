---
title: "Data Fundamentals"
date: 0
hero: /images/posts/writing-posts/git.svg
menu:
  sidebar:
    name: Data Fundamentals
    identifier: cart-fund
    parent: UAGIS
    weight: 30
---

# ESRI: Building maps with UAS Data
### Objectives
  The objective of this article is to inform the reader of basic cartographic skills and how a little bit of domain knowledge can borders the difference between making and missing a GIS project.

### Overview
Proper cartographic skills are imperative to meeting the gold standard for operating with UAS data. From the fundamentals such as turning either a drawing or an aerial image into a map, proper translation techniques and methods (e.g. same geoid, recognition of metadata, XYZ/ZYX) and proper identification markers on the map distinguishes the map as a tool and not a wall photo.

Being able to reference spatial patterns and recognize ground sample distances and digital surface models can inform the user of a host of information relevant to their geospatial project, which is essentially the backbone to use of unmanned aerial vehicles. 

### File Management
Capturing data can be a blast. Without a typical or straight-forward file structure to find the data you captured, though, your enjoyment can turn to dismay once you realize you need to find a specific .csv buried in one of your many, many DCIM folders. For that reason, I am sharing my general file naming logic.

Key characteristics I use are first and foremost the date of flight, in year-month-date foramt. After doing so, I write the location of the job. If there's any initial data, I place the type of flight conducted. This is a format I carried over from when I was big on photography, and I find it incredibly useful. In sorting this way, as your skills (and ideally job list) grow, you can easily find a specific job and the metadata attaached to it. Here's an example of my file structure:

```
+-- 2021-04-22_Martell_3DM
|   +-- 3DM_Captures
|       +-- DCIM
|   +-- metadata.csv
+-- 2021-04-12_PWA_GCP
|   +-- DCIM
|       +-- 01.jpg ...
|   +-- metadata.csv
```

### Metadata
Equally important as the data captured is the metadata of a conducted flight. Without proper reference for geoid or coordinate system, data you captured on one Indiana might end up being processed and referenced as data from the Philippenes. If you were _supposed_ to be in the Philippenes, you might be able to see this as a good thing; chances are, however the data was meant to be captured in Indiana, and the individual you're flying for wouldn't be happy for paying for an NDVI analysis of what apppears to be a random field in Luzon.

When capturing metadata, here is a typical example of the information I take note of **before flying**:

#### FLIGHT INFORMATION	
Location:	Martell Forest
Date:	22 April 2021
Time:	12:37
#### WEATHER	
METAR Used:	KLAF
Temperature:	48degF
Precipitation:	0%%
Winds:	12kt Gusting, West
#### VEHICLE INFORMATION	
Vehicle:	DJI Mavic Pro 2
Sensor:	Ibid
Battery Count:	2
#### MISSION SPECS	
PIC:	Bryan Jacobs
VO:	[Cole Bramel](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=&cad=rja&uact=8&ved=2ahUKEwiY6dzR66jwAhVpGDQIHYOXAGEQFjAAegQIBhAD&url=https%3A%2F%2Fwww.linkedin.com%2Fin%2Fcole-bramel-4481b4153&usg=AOvVaw3P2wpiHmQLRYHAJA7lm7E-) (plug: spectacular PIC for hire!)
Flight Number:	4 22 #2
Takeoff Time:	1237
Landing Time:	1259
Altitude:	8m
Sensor Angle:	-90deg; variant
Overlap:	80%
Sidelap:	80%
Coordinate System:	WGCS 1984 UTM Zone 16

I typically find this information incredibly handy in post-aggregation and when writing reports to ensure my operation doesn't blow up in my face for not knowing what I did.

### Conclusion
No metadata = no mission
Losing your data = no result
Keep track of your flights and it'll show with your track record of excellence.




###### This assignment was written following [Dr. Joseph Hupy's](https://polytechnic.purdue.edu/profile/jhupy) guidance and acts as half of a deliverable for a Cartographic Fundamentals assignment. 