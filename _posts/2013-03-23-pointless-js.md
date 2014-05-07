---
layout: post
title: Pointless.js
created: 1364045132
author: adi
permalink: js/pointlessjs
tags:
- JS
- backbone.js
---
<p><b id="internal-source-marker_0.15754120983183384" style="color: rgb(0, 0, 0); font-family: 'Times New Roman'; font-size: medium; font-weight: normal;"><span style="font-size: 15px; font-family: Arial; background-color: transparent; vertical-align: baseline; white-space: pre-wrap;">Backbone.js is a pointless piece of code!</span></b><br />
	<b id="internal-source-marker_0.15754120983183384" style="color: rgb(0, 0, 0); font-family: 'Times New Roman'; font-size: medium; font-weight: normal;"><span style="font-size: 15px; font-family: Arial; background-color: transparent; vertical-align: baseline; white-space: pre-wrap;">If you need a framework for your web application, do yourself a favor and stay away.</span></b></p>
<p><b id="internal-source-marker_0.15754120983183384" style="color: rgb(0, 0, 0); font-family: 'Times New Roman'; font-size: medium; font-weight: normal;"><span style="font-size: 15px; font-family: Arial; background-color: transparent; vertical-align: baseline; white-space: pre-wrap;">You&#39;re probably wondering about how this can be true, right? I mean, after all, there must be a reason behind Backbone&rsquo;s success... Well, of course there&rsquo;s a reason. It is one that JavaScript developers don&rsquo;t like hearing but still -</span></b></p>
<p dir="ltr" style="margin-top: 0pt; margin-bottom: 0pt;"><b id="internal-source-marker_0.15754120983183384" style="color: rgb(0, 0, 0); font-family: 'Times New Roman'; font-size: medium; font-weight: normal;"><span style="font-size: 15px; font-family: Arial; background-color: transparent; vertical-align: baseline; white-space: pre-wrap;">The reason behind Backbone.js success is, mostly, the ignorance of its users.</span></b></p>
<p dir="ltr" style="margin-top: 0pt; margin-bottom: 0pt;"><b id="internal-source-marker_0.15754120983183384" style="color: rgb(0, 0, 0); font-family: 'Times New Roman'; font-size: medium; font-weight: normal;"><span style="font-size: 15px; font-family: Arial; background-color: transparent; vertical-align: baseline; white-space: pre-wrap;">That&rsquo;s right! When is comes to design patterns and coding best-practices, the average JavaScript developer is a layman.</span></b></p>
<p dir="ltr" style="margin-top: 0pt; margin-bottom: 0pt;">&nbsp;</p>
<p dir="ltr" style="margin-top: 0pt; margin-bottom: 0pt;"><b id="internal-source-marker_0.15754120983183384" style="color: rgb(0, 0, 0); font-family: 'Times New Roman'; font-size: medium; font-weight: normal;"><span style="font-size: 15px; font-family: Arial; background-color: transparent; vertical-align: baseline; white-space: pre-wrap;">You see, JavaScript developers are used to working with libraries, not infrastructures. There&rsquo;s a big difference! Take for example jQuery. jQuery helps you with cross-browser abstraction and keeping your code shorter, simpler, and more readable than if you were writing it using the native JavaScript API. But jQuery is not an infrastructure.</span></b></p>
<br />
<p dir="ltr" style="margin-top: 0pt; margin-bottom: 0pt;"><b id="internal-source-marker_0.15754120983183384" style="color: rgb(0, 0, 0); font-family: 'Times New Roman'; font-size: medium; font-weight: normal;"><span style="font-size: 15px; font-family: Arial; background-color: transparent; vertical-align: baseline; white-space: pre-wrap;">If libraries help closing gaps and filling holes, infrastructures serve as the foundation of applications. They are meant to help you maintain a sane, well formed, and scalable code base. Backbone won&#39;t do this for you. On the contrary! The lack of clear separation between areas of responsibility often, even though unintentionally, encourage you to cook spaghetti.</span></b></p>
<br />
<p dir="ltr" style="margin-top: 0pt; margin-bottom: 0pt;"><b id="internal-source-marker_0.15754120983183384" style="color: rgb(0, 0, 0); font-family: 'Times New Roman'; font-size: medium; font-weight: normal;"><span style="font-size: 15px; font-family: Arial; background-color: transparent; vertical-align: baseline; white-space: pre-wrap;">Luckily enough for Jeremy Ashkenas, all of this doesn&#39;t really matter because common JavaScripters can&#39;t tell the difference... For them, separation of concerns is nothing but a funny term that comes from the boring world of server side development (or something like that).</span></b></p>
<p dir="ltr" style="margin-top: 0pt; margin-bottom: 0pt;">&nbsp;</p>
<p dir="ltr" style="margin-top: 0pt; margin-bottom: 0pt;"><b id="internal-source-marker_0.15754120983183384" style="color: rgb(0, 0, 0); font-family: 'Times New Roman'; font-size: medium; font-weight: normal;"><span style="font-size: 15px; font-family: Arial; background-color: transparent; vertical-align: baseline; white-space: pre-wrap;">Take a look at this quote from Backbone&rsquo;s site:</span></b></p>
<br />
<p dir="ltr" style="margin-top: 0pt; margin-bottom: 0pt;"><b id="internal-source-marker_0.15754120983183384" style="color: rgb(0, 0, 0); font-family: 'Times New Roman'; font-size: medium; font-weight: normal;"><span style="font-size: 15px; font-family: Arial; background-color: transparent; vertical-align: baseline; white-space: pre-wrap;">&ldquo;Different implementations of the Model-View-Controller pattern tend to disagree about the definition of a controller.</span></b><b style="color: rgb(0, 0, 0); font-family: 'Times New Roman'; font-size: medium; font-weight: normal;"><span style="font-size: 15px; font-family: Arial; background-color: transparent; vertical-align: baseline; white-space: pre-wrap;"><span style="color:#ff0000;"> If it helps any, in Backbone, the view class can also be thought of as a kind of controller</span>, dispatching events that originate from the UI...&rdquo;</span></b></p>
<br />
<p dir="ltr" style="margin-top: 0pt; margin-bottom: 0pt;"><span style="color: rgb(0, 0, 0); font-family: 'Segoe UI', 'Lucida Grande', 'Helvetica Neue', sans-serif; font-size: 15px;">If this isn&rsquo;t a red light then what is?</span></p>
<p dir="ltr" style="margin-top: 0pt; margin-bottom: 0pt;">&nbsp;</p>
<p dir="ltr" style="margin-top: 0pt; margin-bottom: 0pt;">&nbsp;</p>