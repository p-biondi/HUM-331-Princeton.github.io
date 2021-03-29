---
layout: post
author: Amna Amin
title: Activism Poster 
---

## Explanation of Thought Process 

The document that I am coding is an image used to advertise an event from Muslim Student Activists. This document is interesting and potentially useful to historians that want to note what topics student activists focused on and how they advertised events. Thus, the aspects of the document that I want to preserve for researchers is noting what titles are used, how information is presented (in forms of questions or demands for instance), where and when these events take place, and images used on the poster. 

Based on the elements I want to document, I want to note the relative size and importance of different elements of the text. For instance, the title can be noted using markup codes like <head>. Additionally, I want to note the group’s hosting so code that includes elements like <orgName> were good markup codes to use. Overall, I also used tags like question to indicate that questions were being asked, date to show a date was given for the event, and location to indicate the physical space the event was held in. 
  
 I think the textual structure used can be similar to that of textual structures used in poems since the poster contains main points and subsections like stanzas. This organization will help show the flow of information and relative importance of each text since the poser itself shows that importance through font sizes and boldness. In particular, I looked at conventions TEI website and saw that div and subsequent numbers like div1 and div2 could show order of importance and emphasis on a document
 
 Some questions that I had about markup while going through this exercise was how to address images within a text. I was not sure if I should just mention that there was an image or offset the image in a tag and then describe what the image was. In general, I was also not sure if the textual structure I used was appropriate and if there was a better one to consider for advertisements and posters. 
 
 ## Example Code 
 
 ```XML

<poster>
	<head>The Migrant Crisis</head>
	<image>Large group of refugees on a boat in the ocean</image>
	<div1>
		<question>What does the word “immigrant” mean?</question>
		<question>How do stereotypes behind the word and 
        formation of national boundaries inform who we think of as immigrants?</question>
	</div1>
	<div2>
		<orgName>Kalaam Cafe:</orgName> A discussion group dedicated to talking 
		about relevant issues in the world. This week, we will discuss the state of 
		immigrants around the world. 	
	</div2>
	<head>
		<date>Friday, May 1, 7:30 PM</date>
		<location>Murray Dodge Room 22</location>
	</head>
	<div2> 
		Sponsored by the 
		<orgName>Muslim Advocates for Social Justice </orgName>
	</div2>
</poster>


```
 
### Citations
 
 To view the original poster image, visit [Archiving Student Activism at Princeton (ASAP) Collection](/http://arks.princeton.edu/ark:/88435/0v8383311) and navigate to the Muslim Advocates for Social Justice and Individual Dignity page.
 
 
 
