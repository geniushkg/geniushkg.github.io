---
title: Augmented Reality &#58 improved perception with camera lenses
date: 2017-09-04 00:00:00 Z
permalink: "/augmented-reality-arcore"
layout: post
---

Improved preception with AR.


**Augmented Reality** : 

A technology that superimposes a computer-generated image on a user's view of the real world,thus providing a composite view.

In layman’s term , just imagine you can also see the real world with extra sensor’s. Your eyes plus thermal imaging capabilities or visualising furniture set up of empty Office, it can be used in almost all fields where it’s difficult to physically place item to check how it looks that can be perceived  without any labour.

**What  Can AR Do ?** 

* Changes the way you shop furniture 
* Renovate your house 
* Select paint color combination for walls
* Or even see your food before it’s prepared , like pizza on empty dish customised for you.

**Lets see it in Action** : 

* Furniture  : 

<iframe width="420" height="315" src="http://www.youtube.com/embed/80trFLZXy5Q" frameborder="0" allowfullscreen></iframe>


* Food :


<iframe width="420" height="315" src="http://www.youtube.com/embed/qnytO7_0q_M" frameborder="0" allowfullscreen></iframe>
 
	
**ARkit** : 

Its Apple’s latest sdk introduced a month ago, that helps developer add augmented reality capablities, as shown in video above.

**ARCore** : 

Its SDK introduced recently by google that helps you  add Augmented reality layer to your camera application. Now lets gets hand dirty playing with SDK.

1. Download sdk from github 
2. Add dependencies and jump into Android studio 
3. Voila , there is no third step, only arcore sdk is single dependency that add layer for motion sensing and learning environment around it. 

	Here’s Bugdroid  on my Table :
	

<iframe width="420" height="315" src="http://www.youtube.com/embed/tOpcDRFJKYA" frameborder="0" allowfullscreen></iframe>

**How Does it works ?**

In computer vision field motion sensing  is bunch of algorithm that co-ordinate video stream input into cartesian graph which detects position relatively to the object.

The sample shown above does. 

1. Detects a flat surface using **Opengls libraries**.
2. Plots and learns environment as and when camera angle changes.
3. Superimpose pre-defined object on co-ordinates


Its in preview (**Alpha** stage),but far more promising to take over future, its estimated to bring drastic change in E-commerce industry.

The key take away is user experience, It helps user experience live products just as physical with comfort to sit at home and avoiding nasty commute.    



