---
layout: post
title: Better Continuous Integration with Git
created: 1269516719
author: ittayd
permalink: alm/better-continuous-integration-git
tags:
- ALM
- git
- CI
---
<p>&nbsp;Git is becoming very popular now, at least for open source projects. I wanted to blog about how Git could be useful for the enterprise.</p>
<p><span class="Apple-style-span" style="font-family: 'Times New Roman'; line-height: normal; font-size: medium; ">
<div style="margin-top: 0px; margin-right: 0px; margin-bottom: 0px; margin-left: 0px; padding-top: 0px; padding-right: 0px; padding-bottom: 0px; padding-left: 0px; font-family: Tahoma, Verdana, Arial, Helvetica, sans-serif; font-size: 75%; font-weight: normal; line-height: 160%; background-color: rgb(255, 255, 255); ">
<p class="MsoNormal" style="margin-top: 0px; margin-right: 0px; margin-bottom: 0px; margin-left: 0px; padding-top: 0px; padding-right: 0px; padding-bottom: 0px; padding-left: 0px; font-size: 14px; font-weight: normal; line-height: 21px; ">There are enough blogs about how you can use Git for private branches, or sharing code between team members without muddling the main repository, so I won&rsquo;t go into that.</p>
<p class="MsoNormal" style="margin-top: 0px; margin-right: 0px; margin-bottom: 0px; margin-left: 0px; padding-top: 0px; padding-right: 0px; padding-bottom: 0px; padding-left: 0px; font-size: 14px; font-weight: normal; line-height: 21px; ">&nbsp;</p>
<p class="MsoNormal" style="margin-top: 0px; margin-right: 0px; margin-bottom: 0px; margin-left: 0px; padding-top: 0px; padding-right: 0px; padding-bottom: 0px; padding-left: 0px; font-size: 14px; font-weight: normal; line-height: 21px; ">Git can also help you achieve better continuous integration.&nbsp;How often have you committed code, after compiling, only to discover the nightly build fails? Usually this is caused by some file you forgot to add to the VCS, or some other dependency that exists on your computer, but not everyone else&rsquo;s.</p>
<p class="MsoNormal" style="margin-top: 0px; margin-right: 0px; margin-bottom: 0px; margin-left: 0px; padding-top: 0px; padding-right: 0px; padding-bottom: 0px; padding-left: 0px; font-size: 14px; font-weight: normal; line-height: 21px; ">&nbsp;</p>
<p class="MsoNormal" style="margin-top: 0px; margin-right: 0px; margin-bottom: 0px; margin-left: 0px; padding-top: 0px; padding-right: 0px; padding-bottom: 0px; padding-left: 0px; font-size: 14px; font-weight: normal; line-height: 21px; ">One of the powerful features of Git is that everyone works on his/her own copy (clone) of a repository. Git is actually a tool for synchronizing repositories, not for synchronizing a working directory and a repository which is what SVN, CVS and the like are.&nbsp;This means every developer can have a repository on a central computer that is monitored by the continuous integration server. When a developer finishes work on a feature, he first pushes his changes to his private repository. The continuous integration server starts a build and the developer is notified if it succeeded or failed. If failed, the developer can fix the issues that caused the failure (without being stressed that others cannot work, as happens in SVN) and repeat the process. When the build is successful, the developer pushes his changes to the central repository.</p>
<p class="MsoNormal" style="margin-top: 0px; margin-right: 0px; margin-bottom: 0px; margin-left: 0px; padding-top: 0px; padding-right: 0px; padding-bottom: 0px; padding-left: 0px; font-size: 14px; font-weight: normal; line-height: 21px; ">&nbsp;</p>
<p class="MsoNormal" style="margin-top: 0px; margin-right: 0px; margin-bottom: 0px; margin-left: 0px; padding-top: 0px; padding-right: 0px; padding-bottom: 0px; padding-left: 0px; font-size: 14px; font-weight: normal; line-height: 21px; ">Here is a diagram of the setup:</p>
<p class="MsoNormal" style="margin-top: 0px; margin-right: 0px; margin-bottom: 0px; margin-left: 0px; padding-top: 0px; padding-right: 0px; padding-bottom: 0px; padding-left: 0px; font-size: 14px; font-weight: normal; line-height: 21px; "><img width="570" height="245" style="border-top-width: 0px; border-right-width: 0px; border-bottom-width: 0px; border-left-width: 0px; border-style: initial; border-color: initial; " alt="" src="/files/Git_CI.png" /></p>
<p class="MsoNormal" style="margin-top: 0px; margin-right: 0px; margin-bottom: 0px; margin-left: 0px; padding-top: 0px; padding-right: 0px; padding-bottom: 0px; padding-left: 0px; font-size: 14px; font-weight: normal; line-height: 21px; ">&nbsp;</p>
<p class="MsoNormal" style="margin-top: 0px; margin-right: 0px; margin-bottom: 0px; margin-left: 0px; padding-top: 0px; padding-right: 0px; padding-bottom: 0px; padding-left: 0px; font-size: 14px; font-weight: normal; line-height: 21px; ">&nbsp;</p>
<p class="MsoNormal" style="margin-top: 0px; margin-right: 0px; margin-bottom: 0px; margin-left: 0px; padding-top: 0px; padding-right: 0px; padding-bottom: 0px; padding-left: 0px; font-size: 14px; font-weight: normal; line-height: 21px; "><span class="Apple-style-span" style="margin-top: 0px; margin-right: 0px; margin-bottom: 0px; margin-left: 0px; padding-top: 0px; padding-right: 0px; padding-bottom: 0px; padding-left: 0px; border-collapse: collapse; line-height: normal; font-size: medium; "><span class="Apple-style-span" style="margin-top: 0px; margin-right: 0px; margin-bottom: 0px; margin-left: 0px; padding-top: 0px; padding-right: 0px; padding-bottom: 0px; padding-left: 0px; border-collapse: separate; font-size: 14px; line-height: 21px; ">The easiest approach to hosting several such repositories is to use tools similar to github. Free ones are&nbsp;<a style="color: rgb(51, 51, 153); margin-top: 0px; margin-right: 0px; margin-bottom: 0px; margin-left: 0px; padding-top: 0px; padding-right: 0px; padding-bottom: 0px; padding-left: 0px; text-decoration: none; " href="http://www.gitorious.org/">gitorious</a>&nbsp;or&nbsp;<a style="color: rgb(51, 51, 153); margin-top: 0px; margin-right: 0px; margin-bottom: 0px; margin-left: 0px; padding-top: 0px; padding-right: 0px; padding-bottom: 0px; padding-left: 0px; text-decoration: none; " href="http://github.com/toolmantim/bananajour">bananajour</a>. These allow creating a &lsquo;mainline&rsquo; repository for people to pull push to and cloning it to private repositories. Using these, Hudson jobs can be created to monitor the repositories and build when necessary.</span></span></p>
</div>
</span></p>
<p>&nbsp;</p>