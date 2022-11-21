> **Warning**
> This page is still under construction, upcoming changes are still being made daily.

## Configuration Files and Tuning Guides for VORON 2.4r2

Having built a VORON is a wonderful experiece, it makes me learn so much about the inner guts of a working 3D printer machine. Having said that, my personal V2 is finally serialized back in March/April. So glad to make it to the VORON community (yay). Kudos and props to all VORON, SuperSlicer dev teams. Also for all the user MODS that the community has provided.

My aim for the printer is to reduce the complexity for me (as a user) and other users so we only need to focus on designing rather than tinkering with our machine all the time.

Not that I am not tinkering with the printer at all, but by setting up all the basic automations that can be done, we are minimizing the downtime and complexity of using the machine.

Don't get me wrong, tinkering will and still be my all-time passion about the machine, but sometimes I wonder if I can make the machine do things that requires minimal interventions from me and that's where this repo comes in.

This repo kinda help me track things down as I do various mods, hardware or software changes that may or may not help others to achieve the same thing.

All of these are based on my specific configurations and machine only and it may or may not compatible with yours. Regardin the quirks and problems, again it's all based on my specific configurations it may or may not present on your config, but it kinda helps me to track down the problems and tune it to be better.

I hope everyone can enjoy and learn more about 3D printers especially with VORONs.

Enjoy...

### Hardware Configurations
- Formbot 300mm3 Kit
- 300 x 300 x 250 mm configured build volume (250mm because of limited Z height)
- Stealthburner toolhead (without the LEDs)
- Clockwork 2 extruder (with  LDO-36STH17-1004AHG for the Extruder Stepper Motor)
- Klicky Probe with Auto Z Calibration Plugin
- Waveshare 4.3 inch touchscreen for KlipperScreen
- Trianglelab Phaetus Rapido HF Hotend with 0.4mm nozzle (built-in nozzle from Rapido)
- LED Bar Clips from [Eddie](https://github.com/VoronDesign/VoronUsers/blob/master/printer_mods/eddie/LED_Bar_Clip/LED_Bar_Clip_Misumi_version2.stl) 
- SUNLU ABS Black and Orange for the colors

## Slicer of Choice
- SuperSlicer 2.4.58.5 -> can be found [here](https://github.com/supermerill/SuperSlicer/releases)
- Most of the parameters are derived from [Ellis's profile](https://github.com/AndrewEllis93/Ellis-SuperSlicer-Profiles) which are already fantastic, but there are some parameters that I would like to configure personally (e.g brim gap, skirt, cooling, flow rate, gcode). 
- Specifically I am using the UHF 30mm3 version of the profile but I think all of them are the same besides the maximum volumetric flow rate (but please do re-check).
- Please note that the profile is tuned for my specific printer only, it may or may not compatible with yours.

## Notes About Ellis's Profile
- The profiles are already great from the get-go, but as always if we want to we can always customize the parameters that are suitable for our needs.
- Make sure we choose the correct speed profiles from the GitHub, there are classified with printers with **Input Shaper** and without and also with the **Maximum Volumetric Flow Rate.**
- For my current setup after tweaking some of the parameters, the printer is printing beautifully without any signs of defects and relatively fast or almost equally fast as the BambuLab X1 Carbon (because I'm comparing the print times in comparison to BambuLab X1 Carbon in BambuStudio)

## Weird Quirks and Problems
#### 1. Sometimes my layer especially on a long infill lines are having a gap 
*Solution : Weird thing is as soon as I change the spool holder from the stock one to the one from Prusa MINI with ball bearing the issue is gone surprisingly.*
- Things I've Tried : 
   - Calibrate PA
   - Calibrate IS
   - Calibrate Extruder
   - Calibrate Flow Rate
   - Check Belt Tensions
   - Check Hotend Clog
   - Check Extruder Teeth

#### 2. Sometimes if my layer height is beyond 0.2mm (e.g 0.25mm or 0.30mm) the layer is not bonding properly and starts to behave like the earlier issue.
*Solution : Don't use layer height above 0.20mm (DUHH) but seriously need to recheck all the parameters again and maybe test other printing geometries.*

#### 3. Z Drift when printing enclosed in an elevated chamber temperature causing the nozzle offset to change during printing.

*Solution : Using Klicky Probe and Auto Z Calibration plug-in seems working when starting the print but not during the print as the frame members expand with temperature. <- need to recheck this again with different chamber temperature and other mods (e.g gantry backers, virtual gantry backers and changing the Relative Reference Index to the far corner of the bed.)*

#### 4. Edges Curling with PLA and ABS

*Solution : This is probably just my materials as with SUNLU or eSUN PLA or ABS, the edges of the print (e.g panel mount for VORONs) are very easy to curl up causing the layer to get very ugly and poor around those steep chamfer overhangs. I am testing with PETG and so far there are no signs of it whatsoever

## Calibrations Steps (In My Own Sequence)
I know there are a lot of guides on the internet and I've followed all of them precisely.
After testing and iterating all the guides for calibrations, I found that these steps are giving me the most accurate results with a logical sequence and requirements.
- [Gantry Squaring](https://github.com/AndrewEllis93/Print-Tuning-Guide/blob/main/articles/voron_v2_gantry_squaring.md) and [De-racking](https://www.youtube.com/watch?v=cOn6u9kXvy0) -< **V2 Specific**
- Belt Tension
   - Some guides are recommending tuning by frequency (e.g 110Hz over 15cm) but I prefer to tune it by feeling and distance measured from the front idler to the other parts (measured using digital calipers). I find this step to be quite accurate and doesn't introduce other varibles such as noises from the fans, motors, and so on.
- Extruder Steps
   - I prefer the hotend to be detached from the extruder when calibrating.  
- Input Shaper
   - Vase mode with manual tuning and some trial and error. 
- Pressure Advance
   - Why pressure advance first? Because PA can reduce the distance of the retractions. That simple.
- Retraction Distance and Speed
   - Built-in calibration from SuperSlicer works very well for me. For me, maximum retraction distance is less than 1mm and 30mm/s speed. 
- Profile Tuning  

## Current Projects (in Progress)
- Making a custom **START** and **END** macros with built-in cooldown and probing logic.
- Conditional Bed Mesh if the printbed is filled with individual piece or by area.
- Filament Change and Pause Macro





<!---
oktavianusricky/oktavianusricky is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
