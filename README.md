This tool is based primaraly on the work described in the article "How to convert a 3D printer to a personal automated liquid handler for life science workflows" in this paper 
they describe the modifications needed in order to convert an Ender 3 3D printer into a platform for automating liquid handling for the purposes of autmating expiermentation 
as well as more generally democratizing self running lab technology.The purpose behind the tool I designed is to further expand access to the same liquid handeling capablity on a morerobust platfrom like the Jubilee 3D, this is is meant to act as an inexpensive alternative to other liquid handeling tools currently available publically on the Jubilee, without requiring new users to modify the tool themselves, the Jubilee spefically is a far more robust movement platform whose prepratary software is purpose built for utilizing a varity of tools which makes the proccess of adding the liquid handeling tool much smoother compared to what can be the fickel proccess of modify the ender.


References:

-Naranbat, D., Phelps, B., Murphy, J., & Tripathi, A. (2025). How to convert a 3D printer to a personal automated liquid handler for life science workflows. SLAS Technology, 30, 100239. https://doi.org/10.1016/j.slast.2024.100239 

-🔬🧪 science jubilee ⚡⚙️#. 🔬🧪 Science Jubilee ⚡⚙️ - Science Jubilee 0.3.2.post1.dev200+gdd7e0ef documentation. (n.d.). https://science-jubilee.readthedocs.io/en/latest/index.html 



# jubilee-3D-Automatic-pipette-tool-
Find here all the necessary resources to build a Pipetting tool for the Jubilee 3D


All necessary components:

# Parts — not included in Jubilee "vitamin kit"

| Quantity | Part / Type                                                          | Notes / Link |
|----------|-----------------------------------------------------------------------|--------------|
| 1x       | Each 3D printed part                                                  | (printed on-demand / repo) |
| 1x       | Captive linear stepper motor (25 mm can-stack captive stepper)        | [Haydon Kerk Pittman product page](https://www.haydonkerkpittman.com/products/linear-actuators/can-stack-stepper/25mm-25000) |
| 1x       | E1 ClipTip — Tip Cone Assembly, Plastic Tip Fitting, single channel, 125 µL | [PipetteSupplies product](https://www.pipettesupplies.com/product/e1-clip-tip-tip-cone-assembly-plastic-tip-fitting-single-channel-125μl-thermo-scientific/) |
| 2x       | M3 button-head screw, **8 mm** long                                   | (not provided in vitamin kit) |
| 2x       | 2-64 × 0.4375" flathead screw                                         | (thread & length per original list) |
| 1x       | SS-5GL limit switch (Omron SS-5GL snap/limit switch)                  |(https://www.digikey.com/en/products/detail/omron-electronics-inc-emc-div/SS-5GL/272367) · 
| 1x       | Jubilee / Generic Extra Tool — "Vitamin kit"                          | (https://www.lukeslabonline.com/products/jubilee-generic-extra-tool-vitamin-kit?srsltid=AfmBOopn3gWTzfLxL6CEZkIZTFIs6pjnynb042KZSuh6t3ffAsHF3te0)


# Jubilee / Generic Extra Tool — "Vitamin kit" (contents)

_Kit product page: Luke’s Lab Online — Jubilee/Generic Extra Tool Vitamins Kit.

| Qty | Item description (as listed on Luke's Lab)         |
|-----:|---------------------------------------------------|
| 2   | M5×60 dowel rod                                   |
| 6   | M3×6 button-head screw                            |
| 4   | M3×10 button-head screw                           |
| 2   | M3×12 button-head screw                           |
| 3   | M3×40 button-head screw                           |
| 6   | M3×8 flathead screw                               |
| 11  | M3×6 flathead screw                               |
| 6   | M5×10 button-head screw                           |
| 9   | M3 heat tapered inserts (heat-set inserts)        |
| 6   | M5 hammer nut                                     |
| 1   | Wiper                                             |
| 3   | M3 threaded 8 mm balls (tool balls)               |
| 2   | O-rings (pair)                                    |
| 1   | Wedge plate                                       |




# Basic assembly instructions:

1.Screw in stainless steel balls with 8mm M3 screws 

2.Use a soldering iron to set the heat set inserts on into the holes for the motor as well as the tool wedge holes. Also set in the heat insert into limit switch trigger 

3.Screw in tool wedge with M3 Screws flat head 8mm long

4.Screw limit switch on the end of the captive motor 

5.Screw in limit switch with 2-64 screws

6.Place tip cone assembly plunger into limit switch 

7.Assemble rest of the tip cone assembly and screw into tool body insuring spring stays in the section with the threading along with both O rings

8.Screw in the motor and make sure the limit switch trigger fits into the slot along the side.

9.-Done

# wiring set up 

1.Each wire is extended approxiamtely 150mm in order to ensure it can comforably operate around the Jubilee 

2.At the end of the wires we will crimp on a Female JST XH 6 pin connecter in this order with the connecter side you are onable to see the crimps through facing away from you 

a. Red to the farthest right port

b. Black to the middle closet to red(skip one port) 

c. Green to the farthest left port

d. Blue to the middle directly next to Black

<img width="593" height="84" alt="image" src="https://github.com/user-attachments/assets/d3635c27-ad4e-4fd0-ba67-cd8e37edd5bf" />

# Automatic Tip ejection:

For any expirment that requires replacing the tips mid operation, we have designed an attachement to the lab automation plate to automaticly
eject tips, the deisgn is based on the same principle as the Naranbat design, and the tip is meant to go inside the basket before jogging over to the head and having 
the head pull down on the spring loaded cone assembly thereby ejecting the tip.

File Name(s): Tip ejction basket and Tip Ejctor Head

Instructions: Assume you are facing the Jubilee with the Y railing point parrallel to where you'r eyes are pointing, and the tool holder facing to your left. 

1.Print both pieces and attach the head to the body using 2 6-32 8mm* long countersink screws 

2.dettach the bed plate L bracket closest to the left corner

3.Using the same M3 screws as the L bracket, screw in the Basket assembly until firmly in place(a little wobble is ok as long as the face the screws go into is flat against the plate) 

4. Create a Macro on the Jubilee and copy this g code script(positions are not exact and you should adjust these to your liking or necessity)
     G90 ;set absolute positioning

     G1 Z185 ;move bed to allow pippette tip to clear all objects on lab plate

     G1 X207 ;moves the pipette within the area of the basket but clear of the ejctor head
     G1 Y280

     G1 Z80 ;moves the bed up so the Ejector head is at the same height as the cone assembly neck

     G1 X287 ;places the ejector head around the neck of the Cone assembly 

     G1 Z90 ; moves ejctor up and then down to eject the tip
     G1 Z80

     G1 X207 ; moves the Pipette away from the ejector neck
   






