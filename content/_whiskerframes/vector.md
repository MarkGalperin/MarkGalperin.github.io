---
layout: "posts"
title: "Whisker Frames: Vector Modeling and MS Work"
collection: whiskerframes
sidebar:
        nav: "wfnav"
author_profile: true
usemathjax: true
gallery1:
  - url: /assets/images/stinker.jpg
    image_path: /assets/images/stinker.jpg
    alt: "placeholder image 1"
  - url: /assets/images/stinker.jpg
    image_path: /assets/images/stinker.jpg
    alt: "placeholder image 2"
gallery2:
  - url: /assets/images/stinker.jpg
    image_path: /assets/images/stinker.jpg
    alt: "placeholder image 1"
---

<!--INSERT A BANNER PHOTO?-->

For my MS thesis, I studied the Whisker Frames mechanism through the lens of algebraic geometry, defining a vector model and visualizing my work using [Desmos](https://www.desmos.com/calculator/sluud6agay), an interactive graphing software. In this simply-defined geometry, I found a property that would come to redefine the system: **all “whisker lines” (green) are tangent to a parabola**. This sparked my interest, and led me to better charactarize the geometry, as shown below.

## System definition

In the vector model, the control frame and face frame are defined as line segments in the {x,y} plane. The face frame is a unit-length line segment on the y-axis, running from the origin (0,0) to the point (0,1). The control frame is a line segment of length s, rotated an angle $$\theta$$ from the y-axis and positioned away from the origin by the vector $$\boldsymbol{r}$$. Because s cannot be changed in the hardware model, it is considered a constant. The position and length of the face frame is also fixed, attributing all degrees of freedom to the control frame. The configuration of the system is thus defined by 3 variables, forming the following **configuration vector** $$\boldsymbol{x}$$...

$$\boldsymbol{x}=\left[r_1,r_2,\theta\right]\in\mathbb{R}^3$$

{% include gallery id="gallery1" caption="HARDWARE MODEL FIGURES, COMPONENT-LABELED FIGURE" %}

## Analytic Solution to whisker orientation

Whisker directions are given by the vector $$ \boldsymbol{u}{(y)} $$. This vector is defined by vector subtraction of corresponding points $$ \boldsymbol{F} $$ and $$ \boldsymbol{C} $$, shown in the figure gallery below. 

{% include gallery id="gallery2" caption="HARDWARE MODEL FIGURES, COMPONENT-LABELED FIGURE" %}

Rearranged, the equation for $$ \boldsymbol{u} $$ is defined below.

$$\boldsymbol{u}\left(y\right)=\ \mathbf{F}\left(y\right)-\ \mathbf{C}\left(y\right)\ =\mathbf{w}y-\boldsymbol{r}$$ 

$$\mathbf{w}\ =\left[s\sin{\theta},1-s\cos{\theta}\right]^T $$

Going forward, I would see the components of $$\mathbf{w}$$ **everywhere** in the geometry.

## Protraction and Spread

In defining an output, I limited my attention to **Protraction and Spread**, two simple measures of whisking motion. 

<!--insert: protraction defn picture-->

**Protraction** is the angle a whisker makes in the dorsal-ventral plane.

**Spread** is the full span of protractions produced by the whisker array. Rats can control the spread of their whiskers as a function of their sensing behavior. **I define spread a bit differently: as the _rate of change_ of protraction** with respect to the distance on the face of the rat.

Analytically, protraction and spread are defined below.

$$\Theta(y)=\ \tan^{-1}{\frac{u_2}{u_1}} = \tan^{-1}{\frac{w_2y-r_2}{w_1y-r_1}}$$

$$\frac{d\Theta}{dy}(y)\equiv\frac{r_1w_2-r_2w_1}{\left[r_1+w_1y\right]^2+\left[r_2+w_2y\right]^2}$$



<!-- ## Modified Vector Model - is this necessary here?-->
<!--Figure: pic of stuff-->

<!--
Say you defined a **constraint** on this system so that the top-most whisker and bottom most whisker followed angles $$\alpha$$ and $$\beta$$, respectively. In such a system, the position ($$\boldsymbol{r}$$) of the control frame would become a function of $$\alpha$$ and $$\beta$$. This constraint, defines the **modified vector model**, where there is still a degree of freedom in $$\theta$$. 

$$\boldsymbol{r}=\left[\begin{matrix}\frac{\tan{\alpha}}{\tan{\alpha}-\tan{\beta}}&\frac{1}{\tan{\beta}-\tan{\alpha}}\\\frac{1}{\cot{\beta}-\cot{\alpha}}&\frac{\tan{\beta}}{\tan{\beta}-\tan{\alpha}}\\\end{matrix}\right]\mathbf{w}=M\mathbf{w}$$

What's cool about this modified model is that it reduces the dimensionality of the system. If given a trajectory of top and bottom whiskers to follow, there's only one variable ($$\theta$$) that needs to be controlled. For this reason, I've called this the _"one degree of freedom (1-DOF)"_ model.

-->

## The Parabola!
I started by asking myself the following question: _where, on the xy plane, can there exist a whisker line?_ Up to this point, my analysis only involved the y-axis (for example, for $$ \boldsymbol{u}{(y)} $$). So, if we were to make whisker lines in the direction of $$ \boldsymbol{u}{(y)} $$, where would those lines reach? Would it be everywhere?

My method was to work backwards: start with a point $$(a,b) \in (x,y)$$ and solve for what value of $$y$$ points $$ \boldsymbol{u}{(y)} $$ in that direction. 

$$y=\frac{w_1b-w_2a+r_1}{2w_1}\pm\frac{\sqrt{w_2^2{a}^2+\left(-2w_1w_2\right)a b+w_1^2{b}^2+\left(-2r_1w_2+4r_2w_1\right)a+(-2r_1w_1)b+{r_1}^2}}{-2w_1}$$

It's a bit messy! But there's one key feature: this is the solution to a **quadratic**, meaning there are either one, two, or no solutions to whether (a,b) has a whisker running through it. This number of solutions depends on the **square root term (discriminant)**. If we set the inside of the square root to zero, it will show us **all values of a and b such that there is only _one_ unique whisker line running though $$(a,b)$$**.

$${\vec{\mathbf{x}}}^TA\vec{\mathbf{x}}=0$$, where $$\vec{\mathbf{x}}=xy1$$ and $$\ A=\left[\begin{matrix}w_2^2&-w_1w_2&-r_1w_2+2r_2w_1\\-w_1w_2&w_1^2&{-r}_1w_1\\-r_1w_2+2r_2w_1&-r_1w_1&r_1^2\\\end{matrix}\right] $$