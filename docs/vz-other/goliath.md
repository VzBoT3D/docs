---
layout: default
title: Goliath hot-end
has_toc: false
has_children: false
permalink: /vz-other/goliath
---

# Goliath hot-end

The Goliath is a high-flow hot-end designed for high-speed printing.

[**Goliath** | VzBoT3D/Goliath](https://github.com/VzBoT3D/Goliath)

## Resellers

List of resellers (this will be updated as the Goliath becomes available). Listed countries or regions are the target region of the webshop or store.

- Mellow Direct: <https://s.click.aliexpress.com/e/_DDPO4TT>
- **Australia:** 
    - [raven3dtech.com.au](https://raven3dtech.com.au/product/mellow-goliath-air-water/)
- **Canada:** 
    - [Northprint3d.ca](https://northprint3d.ca/product/vzbot-mellow-goliath-lsd-hotend/)
- **Denmark:** 
    - [3DO.eu](https://3do.eu/) 
- **Germany:** 
    - [CR-3D.de](https://www.cr3d.de/)
    - [Meltbro](https://meltbro.de/mellow-vzbot-awd-330-3d-drucker-bausatz-metall-komponenten-golitath-hotend-hextrudort.html)
    - [F3D Racing](https://f3d-racing-fdm.myshopify.com/)
- **Poland:** 
    - [X3Dshop](https://x3dshop.com/products/drukarka-3d-mellow-vzbot-330-kit-1)
- **United States:**
    - [Provok3D](https://provok3d.com/vzbot-2/?v=0a10a0b3e53b)
    - [3Dprintedprinter](https://3Dprintedprinters.com) 
    - [Genericprinter](https://www.genericprinter.com/product/goliath-air-water-v2-hotend/)
    - [Print3Dshop.org](https://print3dshop.org/)
    - [Fabreeko](https://www.fabreeko.com/collections/hot-ends/products/vz-bot-goliath-hot-end-by-mellow)

## Assembly & disassembly

The Goliath is assembled in roughly this order:

1. Heater wire around the hot block
2. Heatbreak inserted into the hot block
3. Heatsink or extruder (as heatsink) placed on to the heatsink

### Heater wire

The Goliath uses a nichrome heater wire as heater for the hot-end hot block. It is quite stiff but can also be bent to shape as desirable or necessary. In some situations, it may be necessary to tweak the way the wire sits. For that, please see the full Goliath documentation: [Readme | VzBoT3D/Goliath]

On the **Vz-Printhead**, you can either send the nichrome wire to the back, under the printhead, or, send it on the right or left side in the front. Sending to the right will keep the "natural" bend of the wire.

![Goliath heater wire on hot block](/assets/images/vz-other/goliath/goliath_nichrome-wire.jpg)
<small>© @adam_the_dev</small>

[Readme | VzBoT3D/Goliath]: (https://github.com/VzBoT3D/Goliath/blob/main/Instructions/README.md)

### Tips for VzBoT Alu printhead:

- There are 3 positions you can use for the heatblock since there are 3 screws/standoffs. So you can rotate the heatblock to your need
- On the Vz-Printhead, you can either send the nichrome wire to the back, under the printhead, or, send it on the right or left side in the front. Sending to the right will keep the "natural" bend of the wire.

- You can add a heat insulation sleeve if you like to give more protection of the nichrome wire that sticks out:
- If you run the Vz-Hextrudort CNC version with the Vz-Printhead, the PTFE tube between Goliath and Hextrudort should be 22mm long
- Make sure everything is tighten properly and once you have it mounted and ready, do 2-3 heat cycle then tight the nozzle to between 1.2-1.4 nm (If you do not have a torque wrench, make sure you do not overtight the nozzle to damage thread on the copper heat block)

### Nozzle and Heatbreak

It is recommended to add some thermal paste/grease between the heatbreak and heatsink for better heat transfer. Do not use boron nitride as it will dry and make it really hard to remove heatbreak from heatsink. Always verify the heatbreak was correctly torqued on the heatblock while you are there.

#### Removing nozzle

Always heat the hotend before removing nozzle (Retract/unload filament before removing nozzle). If you do not heat it, harden plastic inside inside the hotend will make it very hard to unsrew, and you can damage the hotend/nozzle 

Only torque the nozzle after you have heaten the hotend. Torque required is between 1.2-1.4 Nm.  
You can use [this tool](https://www.thingiverse.com/thing:4738816) for this.

#### Removing heatbreak

To remove the heatbreak, you will have to heat the hotend first to melt the plastic inside first. This can be challenging. Wear protective gloves to avoid burning yourself. 

Steps:

- remove the hotend from the the printhead
- remove the  Pt1000 sensor
- remove the sock
- unscrew the 3 M2 screws to remove the heatsink
- once heatsink is removed and heatbreak is accessible, use a heatgun, or a blow torch to heat arround the heatbreak (be careful not to heat it too much if you use a propane torch). You want to bring it hot enough to break loose the plastic inside, and it will be easier to unscrew. If you don't have a heatgun or a blowtorch, you can connect the Goliath back to the printer and heat it from the printer. Hold the Goliath by the wire doing so.
- Use a 5.5mm wrench or adjustable one. (There is one provided with the Goliath, but if you can use a better one one that has larger contact, it will give better grip.) And use a 9mm wrench to hold the heatblock at the bottom. This will be tricky, but with care it should unscrew relatively easy.
- install the new heatbreak. Use 1.0-1.2 Nm


### High temp Wire sleeve:
- https://amzn.to/3G2ARA9
- https://s.click.aliexpress.com/e/_DnpvQbp

### Example showing it on the right side.

<img width="587" alt="image" src="https://user-images.githubusercontent.com/37383368/211330774-17573318-2ac8-4077-9e59-f4db8dd18e41.png">


Example showing it in the back, going under the printhead.
![image](https://user-images.githubusercontent.com/37383368/208245292-aa2bffb6-cb29-4fb6-96e3-291e09dfa14b.png)


![20221107_205407](https://user-images.githubusercontent.com/37383368/207979093-63196e0d-56f3-424a-982e-e1408709f36a.jpg)
![20221107_205417](https://user-images.githubusercontent.com/37383368/207979099-c6cb17ce-aef3-4f82-851b-9f2643172785.jpg)
![20221107_205449](https://user-images.githubusercontent.com/37383368/207979102-fba86465-7fe5-4680-8fc2-2dcbefa9aa84.jpg)
![20221107_205648](https://user-images.githubusercontent.com/37383368/207979107-f9026d3d-9ea8-4a57-a937-56f9bd4a0955.jpg)
![20221107_213040](https://user-images.githubusercontent.com/37383368/207979109-92774b52-75a1-4881-99ba-b982ff06326d.jpg)
![20221107_220011](https://user-images.githubusercontent.com/37383368/207979116-aab0bb29-bc96-4824-a3e9-ac4392a51665.jpg)
