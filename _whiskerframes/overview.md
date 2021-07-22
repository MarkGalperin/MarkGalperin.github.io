---
layout: "posts"
title: "Whisker Frames: Overview"
collection: whiskerframes
sidebar:
        nav: "wfnav"
author_profile: true
usemathjax: true
gallery1:
  - url: /assets/images/whiskerframes/image4.png
    image_path: /assets/images/whiskerframes/image4.png
    alt: "placeholder image 1"
  - url: /assets/images/whiskerframes/image7.png
    image_path: /assets/images/whiskerframes/image7.png
    alt: "placeholder image 2"
  - url: /assets/images/whiskerframes/image6.png
    image_path: /assets/images/whiskerframes/image6.png
    alt: "placeholder image 2"
gallery2:
  - url: /assets/images/stinker.jpg
    image_path: /assets/images/stinker.jpg
    alt: "placeholder image 1"
  - url: /assets/images/stinker.jpg
    image_path: /assets/images/stinker.jpg
    alt: "placeholder image 2"
---

![banner](\..\assets\images\notbad2.jpg){:class="img-responsive"}

The SeNSE Lab of Dr. Mitra Hartmann aims to replicate the versatile activesensing behavior of **whiskers** in rats and mice, designing artificial whiskers that **give robots a sense of touch**. An important component of rodent whisker sensing is the ability to move their whiskers, a process known as “whisking”. 

I was given a challenge in abstract: “Improve the way we move whiskers” . This led me to **design, simulate, build, and present a biomimetic mechanism** that not only replicates real biology, but proposes a new perspective on the study of neural control in rodents. This work was the topic of my MS thesis, and I’m currently adapting the work for publication.

## Inspiration and Concept

The lab’s previous method of robotic whisking involved columns of whiskers, each actuated by its own motor. This was costly and space-inefficient. 

I found inspiration in the parallel motions of multiple layers of tissue running through whisker follicles. Unlike our robot, whiskers are biologically actuated in rows.

{% include gallery id="gallery1" caption="MOOSERAT PHOTO, DORFL FIGURE" %}

**Whisker Frames is a mechanism that controls the row-wise orientation and distribution of a whisker array by the free motion of a “control frame” (CF)**

{% include gallery id="gallery2" caption="HARDWARE MODEL FIGURES, COMPONENT-LABELED FIGURE" %}



## Read more
<!--Links to the other pages. Re-format?-->

[Build and physical design iteration]

[Vector modeling and MS work]

[Generating trajectories from biological data]

[Ongoing and future work]

## Check out my thesis defense!
{% include video id="1yo4y2-628qtDLzm9yp3OjhTWhEVv-3ea" provider="google-drive" %}
Read the written thesis [here](/MSThesis.pdf/)

<!--Link targets-->
[Build and physical design iteration]: /whiskerframes/build/
[Vector modeling and MS work]: /whiskerframes/vector/
[Generating trajectories from biological data]: /whiskerframes/optimization/
[Ongoing and future work]: /whiskerframes/future/

