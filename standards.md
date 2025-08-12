---
title: Standards
layout: default
---
# Standards

> _**This file contains all the required standards for components to get it accepted into the Datapack.**_


# SECTION 1: PORTS
## Port Format
All ports will be named in this format:

`[DIR][TYPE]-[#PORTS][ROLE]`

### How the format works:

- **[DIR]** > Can be either an Input, Output, or Bidirectional port (Labelled I, O or B) Bidirectional port holes don't exist for redstone ports yet, but do for item ports.
- **[TYPE]** > BIN (Binary) / HEX (Hexadecimal)
- **[#PORTS]** > The number of ports it has, as a number. If it only has 1 port, you don't have to include this tag! _(e.g. Just BIN instead of BIN-1)_
- **[ROLE]** > Most ports will be SD (Standard), but ports with specific roles will have different colors and have a different named tag. For example, HEX-STATE. If the port is SD you don't have to include this tag! _(e.g. just HEX instead of HEX-SD)_

## Port compliance ratings

- **Compliant:** A port/component that is completely compliant!
- **Semistandard:** Incompatible with some ports, or a less used/more niche version of something else, or a separate size.
- **Extended Semistandard:** Compliant/semistandard but it is allowed to include modded blocks/items/entities.  An example would be create rotational power based ports or components.
- **Noncompliant:** It's not compliant as it doesn't fit under any other categories, does something already done but way way worse, or completely useless.

## Redstone Port Types

- Each port would have a corresponding colored concrete block under it. 
- Locations of the port holes are in (X, Y), in which (1, 1) is the bottom left block on a 16x16 face looking from the side of a chunk. _(Clarification: Port HOLES, not the concrete position)_
- Some ports are "dangerously incompatible," meaning the port's position overlaps with a different, more prioritized port(s), which can cause issues when next to these ports.


### BIN
- **Color:** 🟥 Red Concrete
- **Made By:** Daxis1
- **Status:** Compliant
- **Location:** IBIN at (7, 2) – OBIN at (10, 2)
- The default port. Used to connect components together, and is the simplest port (as it does not preserve signal strength). These are made for speed.

### HEX
- **Color:** 🟦 **Blue** Concrete _(To clarify, **REGULAR** BLUE, not light blue)_
- **Made By:** gingrspacecadet
- **Status:** Compliant
- **Location:** IHEX at (5, 2) – OHEX at (12, 2)
- A more advanced port. They preserve the signal strength from the output of the previous block. Useful for HEX calculations.
- Recommended to have IHEX next to an IBIN to ensure compatibility with other components (IBIN would set the input on that side to 15 or 0 to convert it to HEX)

### HEX-STATE
- **Color:** 🟩 Green Concrete
- **Made By:** guigui, Spin4team4096
- **Status:** Compliant
- **Location:** IHEX-STATE at (5, 4) – OHEX-STATE at (12, 4)
- (Under development) Used to check the state of a component which is currently doing an operation. The component can decide what signal strength each state is. If a component decides multiple states counts as the same value it should pulse when changing between them to indicate the state has changed (But try avoid having multiple states output the same thing). (Examples: A comparator could return the value of the state; an observer can "observe" the state to know if it has changed). You could use this output to make your bigstone circuit do certain things!

### HEX-2
- **Color:** 🟨 Yellow Concrete
- **Made By:** LimeLight
- **Status:** Compliant
- **Locations:** IHEX-2 at (7, 6) and (9, 6), OHEX-2 at (8, 6) and (10, 6)
- Just like HEX, but carries double the amount of data, meaning it can carry 8 bits (1 byte) of data!

### BIN-LR
- **Color:** 🟦 **Cyan** Concrete
- **Made By:** Spin4team4096
- **Status:** Compliant
- **Locations** IBIN-LR at (2, 3) for 1st bit, and stack upwards for every additional bit e.g. (4, 3), (6, 3) and so on, up to 8 bits (e.g. BIN-8LR). OBIN-LR at (14, 3) for 1st bit, and stack upwards again.
- Useful for computational components, especially since most computational circuits are vertical, so you can easily plug it right in!

### BIN-8
⚠️ **Dangerously incompatible next to:** 🟥BIN, 🟦HEX, 🟦BIN-LR, 🟫RAIL (wow that's a lot)
- **Color:** 🟧 Orange concrete
- **Made By:** Limelight
- **Status:** Semistandard
- **Locations:** Coming soon
- Carrys 8 bits of data, but is huge, so a wire can only be one way. However, it can be useful for speed over a long distance of wires, and can also save space within a component since you don't need to fit a HEX decoder inside your components if it uses BIN-8 instead. 

### SOUND
- **Color:** 🟪 Purple Concrete
- **Made By:** BastienA, Xoliks
- **Status:** Compliant
- **Location:** ISOUND at (7,4) – OSOUND at (10,4)
- A wireless port using sound and skulk sensors to transfer data.

### RAIL
**WARNING:** Make sure you put these next to components that use the same type of minecart. Otherwise minecart types can mix and cause issues.
- **Color:** 🟫 Brown Concrete
- **Made By:** Spin4team4096
- **Status:** Compliant
- **Locations:** IRAIL at (8, 2) – ORAIL at (9, 2)
- The IRAIL is regular rail, and ORAIL is powered rail. This port can be used to transfer items (or mobs/players) using minecarts.

![Locations of each of the ports](https://raw.githubusercontent.com/BigstoneDevelopment/datapack-wiki/main/assets/bigstone_ports_new.png)

# Item Port Types
- Each port is a 2x2 space in the middle of a block, and can be on all sides. It's not labeled with a color since you can easily see if it uses water or hoppers.
- **All Made By:** Diax
- **All Status:** Compliant

### ITEM-HOPPER
- **Side Locations:** 
- BITEM > The left side of the port is input hoppers, and the right side of the port is for output hoppers. 
- IITEM > The whole port uses input hoppers.
- OITEM > The whole port uses output hoppers.
- **Top/Bottom Locations:**
- IITEM > Top of the block.
- OITEM > Bottom of the block.
- Transports items using hoppers. Recommended to use BITEM on the sides as it is multidirectional. If you want speed, try to use ITEM-WATER instead of IITEM/OITEM-HOPPER when possible

### ITEM-WATER
- **Side Locations:**
- IITEM > Water flowing inwards 
- OITEM > Water flowing outwards
- **Top/Bottom Locations:**
- IITEM > Top of the block.
- OITEM > Bottom of the block.
- Transports items using water streams. It is faster, but unlike ITEM-HOPPER, it cannot be multidirectional on the sides.

_IMAGES COMING SOON_

# Mediumstone Port Types
- Mediumstone is a variant of Bigstone, but the components are 8x8x8 instead of 16x16x16. Because of this, they use a different port system.
- They use the same colors as their Bigstone counterparts (to save color slots), but they are in different locations.
- Since Mediumstone is a different system to bigstone, overlapping ports with Bigstone is obvious and will not be included in the descriptions.
- A lot of Medium ports do overlap with other Medium ports as there is limited space. This will be included in the descriptions.  

### MBIN
⚠️ **Dangerously incompatible next to:** 🟦MHEX
- **Color:** 🟥 Red Concrete
- **Made By:** GameCobra
- **Status:** Semistandard
- **Location:** IMBIN at (3, 2) – OMBIN at (6, 2)
- The Medium version of the BIN port.

### MHEX
⚠️ **Dangerously incompatible next to:** 🟥MBIN
- **Color:** 🟦 **Blue** Concrete _(To clarify, **REGULAR** BLUE, not light blue)_
- **Made By:** GameCobra
- **Status:** Semistandard
- **Location:** IMHEX at (3, 2) – OMHEX at (6, 2)
- The Medium version of the HEX port.

# SECTION 2: NAMING SCHEME
When sharing a component, try to stick to this format:

[Component name]  
[Description here]  

North: OHEX  
South: IBIN, IHEX  
East: IBIN  
West: IHEX  

You could also represent this with a diagram, with colored arrows. Input arrows would point towards the block, output would point away from it. Here's the above example, this time as a diagram:  
![component diagram example](https://raw.githubusercontent.com/BigstoneDevelopment/datapack-wiki/main/assets/diagram_example.png)

# SECTION 3: RULES  
NOTE: Not all the rules are here yet  
- **components need to be able to work when suspended in the air.** This means that no redstone can be placed at y level 1 since its support is out of bounds.
- **components cannot power things outside of it other than through ports** to prevent accidental conflict. So don't power blocks through roofs or walls.
- **modded components can have a status of extended semistandard at the highest** to prevent confusion and make sure people don't try to use them with vanilla.
                      

_Last updated: 12/08/2025 at 18:03:00.474 UTC_
