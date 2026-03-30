# A Windows and Linux PC Optimizations Guide


## WINDOWS

## Steam Launch Options
  - `-threads x` Adjust the amount of threads the game uses. Replace with your thread count -1 or try half your thread count.
  - `-high` Tells windows to run your game in High Priority mode.
  - `-vulkan` Makes the game run under Vulkan rendering pipeline.
  - `-dx11` Makes the game run under DX11 rendering pipeline.

**Improve 1%/0.1% Lows:**

• **__Process Lasso:__** Using this program, you can force apps to run in a specified priority, as well as adjust core affinity according to your system. [DOWNLOAD](https://bitsum.com/) 

  - You can use this [tutorial](https://www.youtube.com/watch?v=xXpnCqXxwz8&) for general use cases, but figuring out the core affinity optimization for your system is going to wield the best results (example: Intel Efficiency Cores)

**__RTSS (Rivatuner Statistics Server):__** Using this program, you can limit your FPS, 3 frames below your refresh rate and significantly improve your 1% lows. [DOWNLOAD](https://www.guru3d.com/download/rtss-rivatuner-statistics-server-download/)

**DEBLOAT**

  - Using [Chris Titus' Windows Debloater](https://christitus.com/windows-tool/) you can customize and debloat windows to your liking by a click of a few buttons.

     - Open Windows Powershell in Administator and paste this in the console _irm christitus.com/win | iex_  and press enter. You can follow his tutorial [here](https://www.youtube.com/watch?v=yKydZFJRzMk&)


## LINUX

**Best Kernals For Gaming**
  - [CachyOS](https://cachyos.org/): Best for latency and overall FPS. I have over a year of experience with this Kernal and highly recommend it over anything else if you are looking for the best gaming compatibility and stability but also have a general understanding of Arch.
  - [Bazzite](https://bazzite.gg/): Best for FPS and ease of use. Has built a strong reputation for being the most like windows without the bloat and with all the scheduling optimizations you'd expect from a gaming focused Linux Kernal.
  - [EndeavorOS](https://endeavouros.com/): A bit more complicated of an Arch based Kernal but after months of driving, I've come to prefer it for both gaming and everyday productivity.

**UPDATING ON LINUX**
  
  -The 3 Kernals I listed above have install/update package scripts preinstalled and it is easily done by using said script and going through the Y/n prompts.
    This includes chipset drivers. ex. GPU/CPU

## Linux Steam Launch Environmental Variables
  - `gamemoderun` Makes the scheduler activate performance mode while gaming, this varaible should always come first. Depending on your Kernal, you may need to install this. Go [here](https://github.com/feralinteractive/gamemode)
  - `ENABLE_LAYER_MESA_ANTI_LAG=1` Enables anti-lag
  - `PROTON_FSR4_RDNA3_UPGRADE=1` Enables FSR4 for RDNA3 GPUs
  - `PROTON_ENABLE_WAYLAND=1` Forces proton to run games under Wayland as a means to replace x11 and improve stability on Linux
  - `MANGOHUD=1` Adds performance metrics to check, must have it installed [here](https://github.com/flightlessmango/MangoHud)
  
