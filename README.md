## Configuration Files and Tuning Guides for VORON 2.4r2
My aim for the printer is to reduce the complexity for me (as a user) and other users so we only need to focus on designing rather than tinkering with our machine all the time.

Not that I am not tinkering with the printer at all, but by setting up all the basic automations that can be done, we are minimizing the downtime and complexity of using the machine.

Don't get me wrong, tinkering will and still be my all-time passion about the machine, but sometimes I wonder if I can make the machine do things that requires minimal interventions from me and that's where this repo comes in.

This repo kinda help me track things down as I do various mods, hardware or software changes that may or may not help others to achieve the same thing.

I hope everyone can enjoy and learn more about 3D printers especially with VORONs.

Enjoy...

### Hardware Configurations
- Formbot Kit 300mm3
- 300 x 300 x 250 mm configured build volume (250mm because of limited Z height)
- Stealthburner toolhead (without the LEDs)
- Clockwork 2 extruder (with LDO pancake stepper motor)
- Klicky Probe with Auto Z Calibration Plugin
- Waveshare 4.3 inch touchscreen for KlipperScreen
- Trianglelab Phaetus Rapido HF Hotend with 0.4mm nozzle (built-in nozzle from Rapido)
- SUNLU ABS Black and Orange for the colors

### Slicer of Choice
- SuperSlicer 2.4.58.5 and can be found [here](https://github.com/supermerill/SuperSlicer/releases)
- Most of the parameters are derived from [Ellis's profile](https://github.com/AndrewEllis93/Ellis-SuperSlicer-Profiles) which are already fantastic, but there are some parameters that I would like to configure personally (e.g brim gap, skirt, cooling, flow rate, gcode). Specifically I am using the UHF 30mm3 version of the profile.
- Please note that the profile is tuned for my specific printer only, it may or may not compatible with yours.

### Notes About Ellis's Profile
- The profiles are already great from the get-go, but as always if we want to we can always customize the parameters that are suitable for our needs.
- Make sure we choose the correct speed profiles from the GitHub, there are classified with printer that are tuned with Input Shaper or not.
- For my current setup after tweaking some of the parameters, the printer is printing beautifully without any signs of defects and relatively fast or almost equally fast as the BambuLab X1 Carbon (because I'm comparing the print times in comparison to BambuLab X1 Carbon in BambuStudio)

### Current Projects
- Making a custom **START** and **END** macros with built-in cooldown and probing logic.
- 


<!---
oktavianusricky/oktavianusricky is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
