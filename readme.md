# A Windows and Linux PC Optimization Guide


## WINDOWS

## Steam Launch Options
  - `-threads x` Adjust the amount of threads the game uses. Replace with your thread count -1 or try half your thread count (aka. Logical processor). You can open Task Manager and check your thread (logical processor) count there. 
  - `-high` Tells windows to run your game in High Priority mode.
  - `-vulkan` Makes the game run under Vulkan rendering pipeline. (Using this with an AMD GPU, may wield much better FPS in most games.)
  - `-dx11` Makes the game run under DX11 rendering pipeline. (Using this with an Nvidia GPU, may wield much better FPS in most games.)

**<ins>Improve 1%/0.1% Lows and Input Latency</ins>**:

• **__Process Lasso:__** Using this program, you can force apps to run in a specified priority, as well as adjust core affinity according to your system. [DOWNLOAD HERE](https://bitsum.com/).

  - You can use this [tutorial](https://www.youtube.com/watch?v=xXpnCqXxwz8&) for general use cases, but figuring out the core affinity optimization for your system is going to wield the best results (example: Intel Efficiency Cores)

• **__RTSS (Rivatuner Statistics Server):__** Using this program, you can limit your FPS, 3 frames below your refresh rate and significantly improve your 1% lows. [DOWNLOAD HERE](https://www.guru3d.com/download/rtss-rivatuner-statistics-server-download/).

**<ins>DEBLOAT</ins>**

  - Using [Chris Titus' Windows Debloater](https://christitus.com/windows-tool/) you can customize and debloat windows to your liking by a click of a few buttons.

     - Open Windows Powershell in Administator and paste this in the console _irm christitus.com/win | iex_  and press enter. You can follow his tutorial [here](https://www.youtube.com/watch?v=yKydZFJRzMk&).

### <ins>Calypto's In-depth Latency Guide</ins>
  - If you have the time, this very long and in-depth guide explains the science behind Latency, and how to improve it [here](https://docs.google.com/document/d/1c2-lUJq74wuYK1WrA_bIvgb89dUN0sj8-hO3vqmrau4/edit?tab=t.0).


## LINUX

**Best Kernel For Gaming**
  - [CachyOS](https://cachyos.org/): Best for latency and overall FPS. I have over a year of experience with this Kernel and highly recommend it over anything else if you are looking for the best gaming compatibility and stability. Best introduction into Arch in my opinion.
  - [Bazzite](https://bazzite.gg/): Best for FPS and ease of use. Has built a strong reputation for being the most like windows like being immutable (can't change important things and break them) without the bloat and with all the scheduling optimizations you'd expect from a gaming focused Linux Kernel.
  - [EndeavorOS](https://endeavouros.com/): A bit more complicated of an Arch based Kernel but after months of driving, I've come to prefer it for both gaming and everyday productivity.

**CPU Scheduler Optimizations by simcasting**
  
  - [Here](https://docs.google.com/document/d/10dqY3L9oH9F0n9wDi0r5P_OYhU3ZaczYwfUMAvC-WhU/edit?tab=t.0) you can find research on CPU scheduling for Linux Kernels done by Community Member: *simcasting*

**UPDATING ON LINUX**      

    The 3 Kernels I listed above have install/update package scripts preinstalled and it is easily done by using said script and going through the Y/n prompts.
    This includes chipset drivers. ex. GPU/CPU

**STRETCH RES ON LINUX**

  - Using LinuxNext's guide you can learn how to get stretch res to work on any game using steam proton launch environmental variables. [Tutorial Here](https://www.youtube.com/watch?v=kKF_6OHXwzg&)
  
## Linux Steam Launch Environmental Variables
  - `gamemoderun` Makes the scheduler activate performance mode while gaming, this varaible should always come first. Depending on your Kernel, you may need to install this. Go [here](https://github.com/feralinteractive/gamemode).
  - `game-performance` Same as gamemoderun but increase I/O priority as well. Preinstalled on CachyOS.
  - `PROTON_USE_NTSYNC=1` Makes proton use alternative syncing method for smoother experiences on Windows based games. Can wield a nice performance boost on CPU intensive games.
  - `PROTON_ENABLE_WAYLAND=1` Forces proton to run games under Wayland as a means to replace x11 and improve stability on Linux.
  - `ENABLE_LAYER_MESA_ANTI_LAG=1` Enables anti-lag
  - `PROTON_FSR4_RDNA3_UPGRADE=1` Enables FSR4 for RDNA3 GPUs
  - `MANGOHUD=1` Adds performance metrics to check, must have it installed [here](https://github.com/flightlessmango/MangoHud).


 # Credits 
  
  [simcasting](https://www.youtube.com/@GreatestToEverDoIt)  |  made the CPU scheduling guide
