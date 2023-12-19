# e3v3se-orca-profile
Profile for Ender 3 V3 SE in OrcaSlicer

I've been tuning my profile in OrcaSlicer for the E3V3SE. By default it is tuned for PLA, so I tweak flow and retraction as Filament overrides.


Things I've focused on:
  - Speed and acceleration decrease - Most stock profiles bump the accel to max which I have found to be too quick for the speeds required.
  - Retraction - Speed and accel greatly decresed from most stock profiles, resulting in MUCH quieter retractions and minimal strining.
  - No Z-hop :) - Helps with stringing.
  - X-Y home - to match endstops
  - Custom bed model - altered priming location to allow more room for printing (explained below)
  - The skirt I use is 2 really slow loops on 1st layer only.
    The reason for this is to reduce the flow after priming so that when beginning the print, the slow initial layers, there is very small chance for
    oozing to occur, this has resulted in outstanding first layers in both PLA and PETG.

For fit and tolerance i've adjusted the X-Y hole and contour offsets slightly. This is based on tuning done with the torture toaster and various ofer model kits.
Torture toaster prints with all parts free and functional down to 0.2mm tolearnace tab - though i've found tolerance on sepperated parts down to 0.05mm-0.1mm.
So these settings are a happy medium between print and place models and toleranced fits.

I've included filament profiles for the 3 main filaments I have used to tune the machine, these might work for you, maybe not :)
Remember to double check your print settings for things like support, brims and skirts. 


**UPDATE 12/12/2023**

  - I have tweaked the "Detraction speed" to 35mm/s to deal with underextrusion at the start of a line, noticed by large gap in z-seam.
  - Added a build-plate model for the V3SE
  - Tweaked the printable area and machine "Start GCODE" to prime outsied of the 220x220 area, as the actual area of the V3 printbed is 235x235
    Essentially a 7.5mm usable border around the 220x220, Seems like the mainboard is compensating for this but is useable for priming etc
    if you provide Negative GCODE positions.
    - Effectively you should now see the nozzle draw its prime line within the graphic on the build-plate (draws it longer)
      meaning any brims or skirts should no longer interfere with the priming line.

  - I HIGHLY ADVISE TO ADJUST YOUR OWN FILAMENT PROFILES!! (and x-y hole/contour compensation)
  - These profiles work for me and haven't had any issues - always watch your first layer, if it's not perfect, the rest of your print wont be :)

**UPDATE 20/12/2023**

  - Disabled "ensure vertical all thickness" - enabled adds time for know notice in print quality or strength. By all means use this as nessacery, but just turning it off by default
  - Default speeds: Yes, the speeds are lower than creality default, main reason is for quality. Feel free to experiment, I have found myself increasing the speeds for parts that
    don't require a good surface finish or dont need to be dimensionally accurate.
  - Added Silk PLA print profile (even lower speeds :)) and filament profile. First time experimenting with Silk PLA - so might not be perfect, but was happy with the initial results.
    Filament used for this profile is eSUN ePLA Silk dual-color
