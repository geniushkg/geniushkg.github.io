---
title: Augmented Reality &#58 improved perception with camera lenses
date: 2017-09-04 00:00:00 Z
permalink: "/augmented-reality-arcore"
layout: post
---

Improved preception with AR.


**Augmented Reality** : 

A technology that superimposes a computer-generated image on a user's view of the real world, thus providing a composite view.

In layman’s term, just imagine you can also see the real world with extra sensors. Your eyes plus thermal imaging capabilities or visualising furniture set-up of empty floor space, can be used in almost all fields where it is difficult to physically place items to check how it looks. Perception becomes less laborious. 

**What  can AR do?** 

It changes the way
* you shop furniture 
* renovate your house 
* select paint color and combination for walls
* or even see your food before it is prepared, like pizza on an empty dish customised for you

**Let's see it in Action** : 

* Furniture  : 

<iframe width="420" height="315" src="http://www.youtube.com/embed/80trFLZXy5Q" frameborder="0" allowfullscreen></iframe>


* Food :


<iframe width="420" height="315" src="http://www.youtube.com/embed/qnytO7_0q_M" frameborder="0" allowfullscreen></iframe>
 
	
**ARkit** : 

This is Apple’s latest SDK introduced a month ago; it helps the developer add augmented reality capablities, as shown in video above.

**ARCore** : 

Google had its own answer to Apple's ARkit. Named ARcore, this SDK helps you add an Augmented Reality layer to your camera application. Let's get our hands dirty playing with SDK.

1. Download SDK from GitHub 
2. Add dependencies and jump into Android Studio 
3. Voila, there is no third step, only ARcore SDK is a single dependency that adds a layer for motion-sensing and learning the environment around it. 

	Here’s Bugdroid  on my desk:
	

<iframe width="420" height="315" src="http://www.youtube.com/embed/tOpcDRFJKYA" frameborder="0" allowfullscreen></iframe>

**How does it works ?**

In a computer vision field, motion-sensing  is a bunch of algorithms that co-ordinate video stream input into cartesian graph which detects position relatively to the object.

The sample shown above:

1. detects a flat surface using **Opengls libraries**
2. plots and learns environment as and when camera angle changes
3. superimposes pre-defined object on co-ordinates


ARcore is still in preview (**Alpha** stage), but being far more promising to take over the future, it is estimated to bring about drastic changes in the E-commerce industry.

The key takeaway is User Experience; simulations of actual products help in making decisions right in the comfort of your home, without the tedium of commuting to the store.      



