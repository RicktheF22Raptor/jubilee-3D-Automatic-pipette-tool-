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




Basic assembly instructions:

1.Screw in stainless steel balls with 8mm M3 screws 

2.Use a soldering iron to set the heat set inserts on into the holes for the motor as well as the tool wedge holes. Also set in the heat insert into limit switch trigger 

3.Screw in tool wedge with M3 Screws flat head 8mm long

4.Screw limit switch on the end of the captive motor 

5.Screw in limit switch with 2-64 screws

6.Place tip cone assembly plunger into limit switch 

7.Assemble rest of the tip cone assembly and screw into tool body insuring spring stays in the section with the threading along with both O rings

8.Screw in the motor and make sure the limit switch trigger fits into the slot along the side.

9.-Done
