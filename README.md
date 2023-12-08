# e3v3se-orca-profile
Profile for Ender 3 V3 SE in OrcaSlicer

I've been tuning my profile in OrcaSlicer for the E3V3SE. By default it is tuned for PLA, so I tweak flow and retraction as Filament overrides.


Things I've focused on:
  - Speed and acceleration decrease - Most stock profiles bump the accel to max which I have found to be too quick for the speeds required.
  - Retraction - Speed and accel greatly decresed from most stock profiles, resulting in MUCH quitier retractions and minimal strining.
  - No Z-hop :) - Helps with stringing.
  - X-Y home - to match endstops
  - Originally I had a custom bed model/texture to address the black buildplate bug. That bug has since been addressed in the 1.8.0 Release
    so reverted the buildplate and texture to default E3V2. If you run into problems in the future my fix was to convert the png to svg and then
    use the E3S1 model but moved the models orgin to FL corner.
  - The skirt I use is 2 really slow loops on 1st layer only.
    The reason for this is to reduce the flow after priming so that when beginning the print, the slow initial layers, there is very small chance for
    oozing to occur, this has resulted in outstanding first layers in both PLA and PETG.

For fit and tolerance i've adjusted the X-Y hole and contour offsets slightly. This is based on tuning done with the torture toaster and various ofer model kits.
Torture toaster prints with all parts free and functional down to 0.2mm tolearnace tab - though i've found tolerance on sepperated parts down to 0.05mm-0.1mm.
So these settings are a happy medium between print and place models and toleranced fits.

I've included filament profiles for the 3 main filaments I have used to tune the machine, these might work for you, maybe not :)
Remember to double check your print settings for things like support, brims and skirts. 
