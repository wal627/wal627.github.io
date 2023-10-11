---
title: "Multimaterial Pliers"
excerpt: "A custom-modeled pair of pliers utilizing both elastic TPU and rigid PLA."
header:
  teaser: /assets/img/Pliers1.jpg
gallery:
  - url: /assets/img/Pliers1.jpg
    image_path: assets/img/Plierss1.jpg
    alt: "placeholder image 1"
  - url: /assets/img/Pliers2.jpeg
    image_path: assets/img/Pliers2.jpg
    alt: "placeholder image 2"
  - url: /assets/img/Pliers3.jpg
    image_path: assets/img/Pliers3.jpg
    alt: "placeholder image 3"
  - url: /assets/img/PliersGif.gif
    image_path: assets/img/PliersGif.gif
    alt: "placeholder gif"
---

# Project Description
The goal of this project was to utilize print-in-place mechanics and dual extrusion 3D printing to create functional pliers. Print-in-place 3D printing is a revolutionary technique that allows for the creation of complex, fully assembled objects in a single printing process, eliminating the need for post-assembly and reducing material waste. This innovation finds applications in a variety of fields, from rapid prototyping to custom medical devices. For instance, in the healthcare sector, print-in-place 3D printing is used to create prosthetic limbs with integrated joints, enhancing patient comfort and mobility. In the automotive industry, engineers utilize this method to produce intricate, pre-assembled parts such as gears and hinges, reducing production time and costs. This technology opens up exciting opportunities for streamlining manufacturing processes across numerous sectors. 


PLA and TPU: PLA (Polylactic Acid) is a rigid and biodegradable material, while TPU (Thermoplastic Polyurethane) is flexible and elastic. Combining these materials can create objects with both structural integrity and soft, flexible components, making them suitable for applications like phone cases with integrated buttons.

PLA and PVA: PLA can be paired with PVA (Polyvinyl Alcohol) support material. PVA is water-soluble and can be used to create intricate, overhanging structures that are easily removed by dissolving in water after printing.

Nylon and TPU: Combining nylon for the rigid parts and TPU for flexible components is ideal for applications like custom shoes, as it provides durability and comfort in a single print.

ABS and HIPS: ABS (Acrylonitrile Butadiene Styrene) can be used with HIPS (High Impact Polystyrene) support material. HIPS dissolves in limonene, allowing for easy removal of support structures, making it suitable for complex, interlocking designs.

PETG and PCTPE: PETG (Polyethylene Terephthalate Glycol-Modified) and PCTPE (Polycarbonate Thermoplastic Polyester) can be combined for projects where a balance of strength and flexibility is required, such as robust, impact-resistant phone cases.

Metal-infused PLA with Regular PLA: Mixing PLA with metal-infused filaments like bronze or copper-infused PLA allows for the creation of parts with a metallic finish or increased weight, enhancing aesthetics or functionality in decorative items and figurines.

These combinations showcase the versatility of print-in-place 3D printing, enabling the fabrication of objects with varying physical properties and functions within a single print job. The choice of materials depends on the specific requirements of the intended application.

For this project, print-in-place was used to combine TPU and PLA in a single print. While different materials would normally require separate prints and a strictly mechanical joint to combine, print-in-place coupled with dual extrusion allows for materials to be printed simultaneously, so the bond is further strengthened by the regular heat fusion that normally joins layers together. 

# Design Rationale 
To create the spring component, I utilized a TPU 95A filament that was elastic enough to stretch in order to close the pliers, and compress back into its original shape to open the pliers. I chose to make the inner geometry of the elastic portion a grid of nine squares, however, the exact geometry is not significant as long as the spring is structurally sound and has enough room in between the supports to deform. The major variable for my design was the thickness of the supports; A thicker center will be more structurally sound, but may not stretch enough to close the pliers assuming a reasonable applied force. On the other hand, a center that is too thin may snap apart entirely when stretched, or not provide enough resistive force to open the pliers up again. With this in mind, I made my center support thickness a parameter while modeling the pliers, so I was easily able to alter  and tested multiple thicknesses until I found the best one, which I found to be about 1mm thick. The other crucial component of this design was the mating spots for the two materials. Since PLA and TPU have very different properties, a mechanical connection between the two was necessary to withstand the forces applied to the joints when using the pliers. For my connection, I used three dovetail joints on each side of the center portion, and used parameters to make modifying these joints quick and easy. While my first iteration was a success, the dovetails could be made larger in order to ensure a stronger bond and better durability. Finally, the handles and jaws of the pliers were simply printed out of PLA because it is inexpensive and rigid. I added empty space in between the handles and jaws in order to decrease the total amount of material in the model, thus decreasing print time.

# CAD Model
<iframe src="https://vanderbilt643.autodesk360.com/shares/public/SH512d4QTec90decfa6e7b6cb6e9695af6ff?mode=embed" width="640" height="480" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>
{% include gallery caption="3D-Printed Phone Holder Gallery" %}
