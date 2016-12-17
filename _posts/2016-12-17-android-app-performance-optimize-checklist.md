---
title: Android Performance optimize checklist
permalink: "/how-to-optimize-android-apps"
layout: post
date: '2016-12-17 05:55:40'
---

##                      **How to build high performance Android apps ?**

First of all before starting how to build high performance android apps lets see
what is bad performance when user gets frustrated and uninstalls the app.

1) Janky UI -  UI is not update smoothly , as per an research anything updating 	in less then  100ms  is  instant  for  humans,  between  100-300ms  its 	working and above 1000ms user gets distracted, context changes.

2)  Then comes Functionality , If the app says something X , and does Y or does not performs
       X task then also user get frustrated.
			
3) Battery Drain , Its major problem in mobile apps , with every year new models launches 
      with larger screen size and more sensors so to take care of battery life is very important.
			
			
### 			**Now how can we improve performance of android apps to eliminate user frustration**


This suggestion mentioned below is hard work of doug sillars , I learnt it from his book 
**[High performance android apps](http://shop.oreilly.com/product/0636920035053.do)**.


**1) UI Optimization :** Crafting xml UI with appropriate care, we can use hierarchy view in android studio to check depth of UI layout, Thumb rule is try to make UI tree horizontally flat rather then nesting it.

The rocket science behind flat structure is that, while runtime android needs to calculate height & width of each view elements so when it gets nested time taken grows exponential. for 3 nesting depth , it will take time to draw 8 elements.

**Re-Measuring** : Incase there is some error while inflating UI first time, runtime will need to remeasure so time is doubled.

**Overdrawing**: Simply overdrawing a background seems to be small task but it does cost performance, any overdrawn view if present must be removed.

**How much time is Valid :** For android device running at 60 fps so each frame gets drwan every 16ms , so if you are anywhere near 12-13ms then its safe other wise jank will be seen.  

Also time consuming task done on **main UI** thread will cause disruption they needed to be handled in background efficiently.

**Sometimes User Perception can be manuplated using UX tricks for time intensive task**


**2) Funtionality :** This is less tricky, just make sure to pass all test case 	and you can rest assure that function of app will be as per expected

**3) Battery :** This is a major part which involves multiple checks, While inspecting power profile some figures came, It shows that maximum battery consumtion occurs in 

- Screen
- Radio Internet
- sensors abusive usage


**Screen-** Unnecessary wake_locks cause battery drain, it should be removed or minimized. When ever possible allow device to goto sleep this will optimize battery consumption.

**Battery Historian-**  This is a tool that allows to visualize maximum battery usage occurence, its kind of log dump visualized, in conjunction to internet data usage history it will probably be maxed used while performing network operation in background scheduled by alarm manager.

To optimize it we can use Inexactalarm manager api , with lolipop device new Jobscheduler api also can come to rescue, so that out network usage is dense in traffic and minimum time we need connection to internet.

**Sensors-** lets assume that GPS data is not available with accurate result still we continuously listen data for 20 minutes will cause a battery drain problem. In context of sensors we need to make balance on amount of data we want to collect and amount of data is really required.

This is minimum list by applying this techniques Google play store ratings can be improved. 

Explaining each of these is not scope of this post but someday you might see a 5 post series on **Building High Performance android apps.**
