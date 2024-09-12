# **What does "Motor on Delta" mean?**
 
An electric motor can be wired in different configurations, with the two most common types being the "Star" (also known as "Y") and "Delta" configurations:

Star Configuration (Y-Configuration):
> In the star configuration, the motor windings are connected so that they meet at a single point. This setup generally provides more torque but results > in a lower top speed. It is commonly used in standard electric scooters because it offers a good balance between power and efficiency.

Delta Configuration:
> In the delta configuration, the motor windings are arranged in a triangle, allowing the motor to handle higher currents. This leads to higher topspeeds > but lower torque compared to the star configuration. The delta configuration is often used in modifications aimed at increasing speed.

What effect does the Delta configuration have on a Ninebot G30?
> Higher top speed: The delta configuration enables the motor to achieve higher RPMs, resulting in a higher top speed for the scooter.
> Lower torque at low speeds: While the motor performs better at higher speeds, it delivers less torque at lower speeds, which may result in slower
> acceleration.
> Reduced heat development: Since the delta configuration allows for higher speeds, it can lead to lower heat buildup in the motor, as opposed to the
> star configuration, which might require field weakening to reach similar speeds, potentially generating more heat.

_**You need the space where the internal charger normally is located!!! This guide is only for the Ninebot G30 with 3Cap ESC, 36V Battery and Gen1 or Gen2 motor**_

## Items you need:
* 3x [Automotive Relays](https://www.ebay.de/itm/164626406625?_trkparms=amclksrc%3DITM%26aid%3D1110006%26algo%3DHOMESPLICE.SIM%26ao%3D1%26asc%3D271354%26meid%3De0e6f90e493447f7a480854b7d21e6db%26pid%3D101875%26rk%3D2%26rkt%3D4%26sd%3D166641677889%26itm%3D164626406625%26pmt%3D1%26noa%3D0%26pg%3D2332490%26algv%3DSimVIDwebV3WithCPCExpansion&_trksid=p2332490.c101875.m1851&itmprp=cksum%3A164626406625e0e6f90e493447f7a480854b7d21e6db%7Cenc%3AAQAJAAABAKAOBbj8c9I6eO4vPyI9FfMl8NhNqsULUU1TfDUZ7khl1HSDWsGPZf%2FJKmRHMx0uvxvIrEITwzyTAZ18AckHeHWS3zKHWq3dn7%2FLjSbcDB0Fp9YWHdq02J9KX6UDfegECSWBzmi99S5rxCnOjalyiKt1PXi3HpCe14xvkf1h62qlM7NCbBjtwl0v7fiL%2FFzi3O1SUTNpPiGprTh0WcQLABdsr%2Fz0BmpKiWRstriCbgyk7jYtwdHdsicbg2vdWjRO%2FZ5ECFe6vW5fYKvX9YiX%2FjUNV9K9MdpB0C4gNoUXyRMriYtdrAGJ0u8f4UGW0BcY4UBBB18M4iOzRgnel65xgjY%3D%7Campid%3APL_CLK%7Cclp%3A2332490&itmmeta=01J7EM64TXBRAE76YAE4S1AP23)
* (Manual self return) [Button ](https://de.aliexpress.com/item/32956189343.html?spm=a2g0o.productlist.main.17.6fa7bHvnbHvnWX&algo_pvid=690af3ee-3f1f-4aca-a3f6-11496ed57244&algo_exp_id=690af3ee-3f1f-4aca-a3f6-11496ed57244-8&pdp_npi=4%40dis!EUR!7.59!7.59!!!58.30!58.30!%402103868a17259972397494284e1d06!66377163805!sea!DE!3133146471!X&curPageLogUid=PjVfckKTBMPr&utparam-url=scene%3Asearch%7Cquery_from%3A)
* 1 meter Motor Phase cables
* cables to enlarge the button cables
* heatshrinks in different colors
* motor phase connectors
* addtional stuff like soldering iron.......

### _**STAR-DELTA Guide**_

**STEP 1:** You begin by disconnecting all cable ends inside of the motor, including hall sensor wires, please take pictures to know which cable connects to which sensor afterwards. Once that's done, you remove the silicon on the axle where the phase wires go out of the motor. After that you remove the cables from the axle. Next step is to dismantle the cable to reuse the hall sensor wires/phase wires (pay attention, dont damage them!). Next step would be to add 3 extra phase wires of your choice (the original ones are 14awg). Keep the current specifications and the space that you need for putting all 6 wires + hall wires through the axle in mind. After you put everything back together, re-solder the original phase wires/hall wires to their original connection. Now, you can open up the connection, where all three copper windings connect, and re-solder these endings of the windings, to the new additional phase cables. After that, you have to use some silicon to avoid water from entering.

**STEP 2:** After you successfully converted the motor, you begin building the switching mechanism. At first you solder all blue wires of the three relays together. After that you solder all red wires to the phase wires of the controller.Important!! Now you have to mark, which relais connects to which phase wire on the controller!!! Put a BLUE heatshrink on the big yellow cable of the relais, which connects to the yellow phase on the ESC, put a YELLOW heatshrink on the big yellow cable which connects to the brown phase on the ESC and put a BROWN heatshrink on the big yellow cable of the relays, which connects to the blue phase on the ESC. Now you can put some connectors (male) on the 3 phase original wires of the motor and 3 connectors (female) on the esc phase wires and 3 connectors (female) on the yellow cables, which you marked with heatshrinks.

**STEP 3:** In the third step you start putting motor and switching mechanism together. You use a circuit analyzer to check, where the new phase wires belong to. Example: "You check if there is connection between yellow phase and addtional wire one, if there is no connection it wont beep. Repeat that step until it beeps and then you know that it belongs do yellow phase. Do this until you know which one is connected to which phase (color)." After you checked that, you mark the additional phase wires too with heatshrinks in the colors blue, brown and yellow and add 3 male connectors to them.
 
**STEP 4:** Last but not least you need to connect the last 6 relay wires in a specific way: connect thin yellow wire of the first relay to the white of the second, connect the thin yellow wire of the second relay to the white wire of the third relay. Now you only have the white wire of the first relay and the yellow wire of the third relay. The white wire is ground, and you connect it via parralel cable to the 36V battery. The Yellow wire connects to the switch, which you can put on your handle bar, you have to enlarge the cables of the switch so you can put them through your scooter to the switching mechanism. You connect the 2 wires, which are not the led of the switch to the last yellow cable of the switching mechanism and the other wire to the battery + red (36V).


**STEP 5:** Enjoy your ride!!

_**If you have any questions, or you want to know more about star-delta,**_
_**you can join the star delta discord server here:**_
[STAR_DELTA DISCORD SERVER](https://discord.gg/KBrA8HTagB)
GERMAN GUIDE ON THE DISCORD SERVER!
