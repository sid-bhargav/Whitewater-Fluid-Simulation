# Whitewater-Fluid-Simulation

## Using My Blend File

I wanted to try to create a fluid simulation in Blender that was more realistic. I added the simulation cache files seperately because unfortunately they turned out to be very large. I wouldn't recommend using it unless you have the 60gb of space needed. My simulation settings have all been plugged in and you can downscale whatever you chose to save some space. Bringing down the resolution divisions should probably do the trick. 

If you're using my cache file, store it in the same location as where you have the blend file and it should work. 

If you want to save on bake time I recommend not baking foam because I actually chose not to use it in my final render.

## Tricks I Used 

I found that the liquid mesh bake was never as detailed as I wanted it. I decided to use a method I discovered with a [previous project](https://youtu.be/3oI_8MdwKiY) and added a noise texture with some distortion to the normal value of the water for the illusion of more detail. 

You'll also notice from the videoe that the spray bake seemed to look like a grid. Althouh I was not able to completely remove this from my bake, I found that by moving the geometry of my spray particles away from the origin, I was able to reduce the effect in the final bake.

I also realized that the spray particles weren't looking as realistic as I wanted because there was no mist. I added the mist by creating a rectangular prism with a principled volume node. I then used a noise texture node to control the emission strength and density.

Finally, in Davinci Resolve I used a photo overlay of some rainbows to add a fog bow which helped with the realism. 
