---
title: "Recycling 3D Printer Head: Introduction, Background Research"
date: '2021-03-20T12:19:00+02:40'
comments: true
noauthor: false
share: true
---
## Why? ##

In 2nd year I made vases and bowls using a modification to the settings of a 3D printer to make surface effects with the layer lines, as you see here:

The reasoning for the project was to show that final products can already be made with cheap 3D printers. The layer lines on 3D printed parts are often seen as ugly and a reason why 3D printers are only good for prototypes. By making the layer lines an attractive aesthetic of the product. 3D printers are made to be an option for creating final, “permanent” objects.

I'm hoping to print these out of recycled plastic and maybe sell them (I am working with the business station about that). I was able to use filament produced from recycled plastic in 2nd year but I would like to print directly from recycled plastic so 	that I have control over the whole process and can experiment with the mixes of plastic.


![](/3D2001.png)
![](/3D2002.gif)



## Then there is the more speculative aspect of the reasoning: ##

If 3D printers are good enough right now to produce at least some "permanent" products, such as vessels, sculptures then:

What if we could produce permanent products from disposable plastics using 3D printers? Either at home or locally?

This would be a more effective, transparent and direct form of recycling which removes single use plastic from circulation and transforms it into something permanent and beautiful which people want to keep. Currently disposable plastic is recycled over and over again. Our current system of recycling makes its money from recycling, and so they have no reason to actually reduce the amount of (disposable) plastic in circulation. Actually, it is the opposite: their profits increase from an increase in waste.

## Why, then? For the common knowledge: ##

Converting recycled plastic to 3D printer filament has been done many times by D.I.Yers and in commercial products but it is expensive and complicated to get into, it is also slow as it adds a step between shredding the plastic and being able to use it again and, most importantly, the filament produced must fit in precise tolerances in order to work properly in 3D printers.

Meaning that reliably producing usable quality filament from inconsistent recycled material is very difficult. Refil was a company producing filament from recycled plastic bottles at Bluecity but had to stop because they couldn’t produce it with a reliable quality.

The pellet extruder, where you feed virgin plastic pellets or shredded, recycled plastic directly into the extruder skips the filament altogether. There are several commercial offerings but they are expensive. There are some D.I.Y pellet extruder designs online but there isn’t a working Open design option with clear documentation available at the moment. The closest I found is: https://homofaciens.de/technics-machines-3D-printer-Granule-Extruder-V2_en.htm
(Detailed further below)








**Needed parts list:**

Blender: To shred the plastic for testing ( will buy from marktplaats or second hand shop) From looking at several granular printers on Youtube, it seems a particle size of <2mm at its widest point is needed to work properly.

*Nozzle:*

Larger diameter = easier to prevent clogging

Can make at metal station

Larger nozzles are less likely to clog from the recycled plastic as long as there is enough heat to keep the plastic flowing properly. My pieces are already printed with 1.5mm nozzles and larger would probably actually be better for my purposes

*Heater:*

“Spiral Heaters” - Heating from all sides of the heating chamber

About them: https://dyzedesign.com/2020/04/spiral-heaters-are-the-next-step-in-3d-printing/#

Current 3D printer heating blocks aren’t optimal, especially for large melting chambers, because they heat from one side. Using the cylinder design of the paste extruder at Digi Lab with a spiral or a band heating element wrapped around the outside could heat all sides evenly.

This is why for high flow or large melting chambers where even heating is important, spiral or radial heaters around a cylindrical heating chamber are preferred.

![](/3D-3.png)




Some industrial thermoplastic extrusion welders us the same method of heating but they use filament not granules like we are going for.

![](/3D-2.png)












There are many options available for heaters which would work with cylindrical heating chambers online:

Flexible coil or “spiral” heater: https://www.alibaba.com/product-detail/Temperature-control-box-with-enail-coil_1600162651788.html?spm=a2700.7724857.normal_offer.d_image.22562f15rod8uK

*Band heaters:*

Brass: https://www.alibaba.com/product-detail/120v-220v-240v-380v-Industrial-electric_62094377504.html?spm=a2700.galleryofferlist_catalog.normal_offer.d_image.220e3f07XFRAZJ

Ceramic:
https://www.alibaba.com/product-detail/220v-induction-heating-element-ceramic-mica_62479663919.html?spm=a2700.galleryofferlist_catalog.normal_offer.d_image.220e3f07XFRAZJ




But I need to figure out how to power and control them and monitor and maintain the temperature, if the 3D printer (an Ultimaker Original) can provide enough power for one of these heaters then I can simply connect it directly to the existing heater terminal on the power supply:


There are many simple heating control projects already with Arduino like this.
https://makezine.com/projects/adjustable-temperature-controller-heating-elements/




**EXISTING “Pellet Extruder” designs:**

“HomoFaciens” Granule Extruder: Very simple design with 3D printed and standard parts only, uses the original extruder stepper and 2 standard 3D printer heating cartridges, so I can just build it quite easily. If it works maybe it is more worth while to develop this design further than modifying the paste extruder (These are enough for the relatively small heating chamber in this design compared to the paste extruder we are trying to modify).

I have started printing this to test it - 10/02/21



Project Page:
https://homofaciens.de/technics-machines-3D-printer-Granule-Extruder-V2_en.htm

![](/3D-9.png)


He uses and recommends screws over drill bits because screws have a lower pitch and are cheaper.
I guess the tighter, less sloping threads make less work for the stepper motor.

But I don’t think that’s true. Using a gear system between an appropriate drill bit and the stepper as has been done with the paste extruder should be fine.

He uses 2 standard RepRap heating elements in a custom Alu heating block and that seems to work. I wonder if it could keep up with larger nozzles and more flow?

Explaining video:
3D files in description. (Bonus: very German accent)
https://www.youtube.com/watch?v=oRNgIu3K7vg

He uploaded a new video since I last checked: https://www.youtube.com/watch?v=Nycx9_I9eec



2. Mahor.xyz  Maker and seller of a pellet extruder - could reverse engineer it or elements of it but it is quite complicated looking.  The website is like a blog with info and projects about printing w/ recycled plastics.

https://mahor.xyz/ - main website

https://mahor.xyz/wiki/pellet-extruder-wiki/ - wiki about pellet extruder including instructions and part list - This design uses a drill bit in a similar design to the Digilab Paste extruder. Also encouraging is that it uses a standard 3D printer heating cartridge and stepper, so it can be added on to most existing 3D printers. Although large nozzles and flow rates may be too much for this heating cartridge I think. The other heating element options I listed above would be a more useful option.

![](/3D-10.png)

https://www.youtube.com/channel/UCttVq8TeX4numdzQCMTInow/featured His youtube shows other experiments with pellet extruders

3. Universal Pellet Extruder - RepRap 3DP by RichRap

Designed to be mostly 3D printed and to use common parts. Working with virgin pellets but not recycled plastic. The plastic is melted as it is being transported to the nozzle by the screw.

![](/3D-1.jpg)


4. "Developing a plastics recycling add-on for the RepRap 3D printer" - TU Delft

https://www.yumpu.com/en/document/read/37333804/reprap-granule-extruder-tudelft1

Experiments in to designing a recycling 3D printer add-on by TU Delft. Interesting is that it is a very simple design they tested. The research paper includes diagrams and citations to their reference projects.

![](\/3DIntro31.png)

5. "Screw Extruder (Posted by goaran) "
https://reprap.org/forum/read.php?180,40735

A short forum post about a prototype attempt at a pellet extruder. What is interesting is their idea to heat the tube with the screw up to the glass point of PLA to soften it and also a regular, hotter heating element just before the nozzle.

Its clear some amount of virgin plastic has to be mixed in with the recycled to get suitable quality prints. Maybe I could add virgin bioplastic instead?

Video showing how % of recycled plastic affects print quality: https://www.instagram.com/p/CCt05JGKGfS/?utm_source=ig_web_copy_link

![](/3D-11.png)


Research Paper about “Evaluation and verification of the virgin–recycled mixing ratio of polypropylene plastic”

https://www.sciencedirect.com/science/article/pii/S2214860418307802
