---
title: "3D-Printed Phone Holder"
excerpt: "A custom-modeled phone holder with adjustable viewing angles."
header:
  teaser: /assets/img/Phone-Holder-3.jpeg
gallery:
  - url: /assets/img/Phone-Holder-1.jpeg
    image_path: assets/img/Phone-Holder-1.jpeg
    alt: "placeholder image 1"
  - url: /assets/img/Phone-Holder-2.jpeg
    image_path: assets/img/Phone-Holder-2.jpeg
    alt: "placeholder image 2"
  - url: /assets/img/Phone-Holder-3.jpeg
    image_path: assets/img/Phone-Holder-3.jpeg
    alt: "placeholder image 3"
---

# Project Description

The main goal of this project was to familiarize myself with top-down modeling, an approach to 3D modeling in which the structure is broken down into components that can each be created and edited without editing the entire structure. As someone with a background in computer science, this approach reminded me of coding repository tools such as GitHub, where each programmer can alter a certain branch of the code risk-free before committing it to the main program. The benefit to this kind of modeling is the ability to not only separate the assembly into components, but work on each component intermittently without the risk of ruining the entire assembly. For example, if I were to create component A, create a second component B, and then realize component A needs significant alterations, I could simply alter component A’s timeline without having to delete and remodel all of component B. For this phone holder, I leveraged top-down modeling by separating each of the seven parts into components and modeling each individually. This allowed me to easily alter different features of each component such as thread size and thickness. By utilizing parameters for features that spanned across components, I was able to further increase the modularity and adaptability of the design.

# Design Rationale 
The rationale for the design was simple; The phone would be clamped in place by a clip and threaded gear, and that assembly would then be placed on a lockable ball-and-socket to offer as many degrees of freedom as possible. The cap of the ball-and-socket is also threaded and can be clamped down to lock the joint into place. Finally, the whole assembly attaches to standard 25mm bike handlebars using heated inserts and M5 screws. Combining the phone clamp, ball-and-socket, and bike clamp, I was able to successfully achieve a phone holder that can fit almost any phone, hold the phone at any reasonable angle, and attach to all standard bike handlebars. I chose to print my phone holder out of PLA for its rigidity, cheap cost, and UV resistance compared to ABS. While materials like carbon fiber were available, these exotic materials can be difficult and unreliable to print, as well as expensive.

# Assembly

There are seven total parts to the phone holder. To assemble it completely, one must first set the M5 heat inserts into the bottom handlebar piece. Then, the bottom of the ball joint socket can be attached to the bike frame with standard M5 screws. The ball piece then can be set in place in the ball joint socket using the joint cap, and the main phone mount can be screwed on top of the joint. Finally, the clip can be placed on the phone mount and the large gear screwed on over top to clamp down onto the phone.


# CAD Model
<iframe src="https://vanderbilt643.autodesk360.com/shares/public/SH512d4QTec90decfa6ed4beca740aae9bb2?mode=embed" width="640" height="480" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>

{% include gallery caption="3D-Printed Phone Holder Gallery" %}
