(Original Message about my Fork, now Discontinued) - The modifications in this fork are meant to supplement D912Pxy's PSO Cache loading to help prevent games from crashing immediately, allowing both ReShade and Depth Buffer support on different D3D9 => DX12 Titles. Updates may be few and far inbetween, but the initial release should allow for most issues to be avoided by using Custom Configurations if the situation arises.

**#####################################################################**

**This fork is now discontinued, you should now use Gshade - See below:**

**#####################################################################**

***Gshade:*** https://gposers.com/gshade/

***Instructions for [Guild Wars 2] Installation:***

- (1.) Run the Gshade installer and when it asks for the game executable, select your [Guild Wars 2] 32 or 64 .EXE

- (2.) When prompted, tell Gshade that Guild Wars 2 is for DX12; if you do not it will be named d3d9.dll instead of the required dxgi.dll - D912pxy must have the name d3d9.dll, not Gshade.

- (3.) After you run through the prompts, go to your Guild Wars 2 folder. 

**#####################################################################**

**If you use UOAOM (Addon Manager) skip 4 and 5. They are for using only Gshade and D912pxy together without other addons.**

**#####################################################################**

- (4.) Everything that Gshade created in your Guild Wars 2 directory must be moved to...

64bit Users: bin64 folder.
32bit Users:  bin folder

*Stuff to move if found:*

  *- gshade-presets*
  *- gshade-shaders*
  *- dxgi.dll*
  *- GShade.ini*
  *- GShade.log*
  *- GSInstLog.txt*
  *- notification.wav*

- (5.) Ensure D912Pxy's d3d9.dll is in bin64 for 64bit Guild Wars 2 or otherwise bin  for 32bit.

- (6.) Within Guild Wars 2, open Gshade (Shift + F2) and proceed until you can open the Settings tab.  Set the Shader and Texture Search Paths correctly as the default is typically incorrect. Go back to Home and click Reload to have the available shaders be redetected.

*Note: You can delete shaders you do not use to reduce clutter, do not delete ReShade.fxh or qUINT_common.fxh.*

*In the Gshade DX12 tab, do not enable Copy Depth Buffer Before Clear Operations as its current implementation will cause crashing.*

*Make sure you're running the latest recommended version of D912Pxy.*

*Latest D912Pxy:*
https://ci.appveyor.com/project/megai2/d912pxy/build/artifacts

**Extra - D912pxy Reduced Graphical Pop-in:**

- (7.) If you want reduced graphical pop-in for game assets with D912pxy, browse to your D912pxy folder and open your config.ini - if this file does not exist, run the game client once and then close it.

- (8.) Locate and change " *load_pso_cache=0* ,  *save_pso_cache=0* " both to 1.

- *This will allow you to save the shaderCache / PSOCache for the game assets after they have been converted to work with DX12.*

*D912pxy Note: Please keep in mind that the more cache you have built up, the longer it will take to boot the game as all assets have to be loaded before the client will open and fully load.  This can take awhile depending on your PC.  The same goes for closing the game, but only if you have encountered a lot of new shaders during your gameplay that time around.*

*Secondly, try to avoid changing your Shaders and Environment settings within Guild Wars 2 as it will overly bloat your shaderCache/PSOCache for D912Pxy as it is a separate set of shaders for everything in the game.  These new shaders will have to be loaded on new restarts even if you do not use the same setting you were at the beginning.*

*Lastly, if you encounter any problems, see if renaming your d912pxy\pck\latest.pck resolves the issue.  After some D912Pxy or Guild Wars 2 updates, this file may have to be removed, thus restarting your shaderCache / PSOCache from scratch.*



**#####################################################################**

**Guild Wars 2 Development Community - https://discord.gg/zqeHCEg**

**megai2's D912Pxy Repository - https://github.com/megai2/d912pxy**

**Original ReShade Repository by Crosire - https://github.com/crosire/reshade**

**#####################################################################**
