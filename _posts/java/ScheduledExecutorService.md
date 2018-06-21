---
title: 中文測試
date: 2013-12-24 23:31:30
categories:
- test/test
tags:
---

最近使用java中的定时任务时，对于标题中的几个方法有点懵，故而记录一下。

schedule(commod,delay,unit) ，这个方法是说系统启动后，需要等待多久执行，delay是等待时间。只执行一次，没有周期性。
举个栗子：火箭发射，delay=10秒，发射准备好了之后，开始读秒：10,9,8，，，1，发射。piu~，任务完成，回家吃饭。

scheduleAtFixedRate(commod,initialDelay,period,unit)，这个是以period为固定周期时间，按照一定频率来重复执行任务，initialDelay是说系统启动后，需要等待多久才开始执行。
举个栗子：高铁定时发车，过时不候；period为一天，以天为周期，优先保证任务执行的频率。

scheduleWithFixedDelay(commod,initialDelay,delay,unit)，这个是以delay为固定延迟时间，按照一定的等待时间来执行任务，initialDelay意义与上面的相同。
举个栗子：【这个例子相当的不好找。。。我后面的同事在玩炉石】就拿炉石传说来讲吧，假设他每玩一局休息10秒钟，然后再开始玩。每开新的一局，打完的时间不是固定的，但是间隔是固定的，就是delay=10秒，表现在时间轴上就是【第一局260秒】【休息10秒】【第二局150秒】 【休息10秒】...【第N局180秒】【休息10秒】。这个是优先保证任务执行的间隔。
感谢：http://blog.csdn.net/yuzjang/article/details/52412003
[转]
