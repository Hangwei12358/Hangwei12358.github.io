---
layout: post
title: "mex issues"
date: 2018-07-06
---
Mex function is really helpful for transforming C/C++ source files into .mexa files for Matlab to use. However it's not trivial sometimes to debug the mex functions due to system architecture and version problems.
Today I encounter a problem when building mex functions. The program is written for i386, aka, x32 system. However mine is i386:x86-64. The system incompatibility caused the following problem.
 
![mex-error](http://Hangwei12358.github.io/img/mex-error.png?raw=true)

Then I tried millions of different methods and tricks found online, and finally it turns out to be really simple to be solved.

> Simply modify the .obj in the code to .o 


As shown in the following screenshot, the commented green code is the previous code, and the uncommented lines are corrected version. Nailed it!
![mex-solution](http://Hangwei12358.github.io/img/mex-solution.png?raw=true)
