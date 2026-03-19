# DXVK.CONF-FILE-SETTINGS-
* This contains light and extreme dxvk.conf settings to tackle and reduce game stutters and heavy lagging.

  
## Usefulness & Key Features
* Extreme Draw Call Management: Utilizes the custom starengine.drawThreshold and starengine.bindSkip parameters to aggressively reduce CPU overhead in crowded game areas.
Bandwidth Optimization: Employs d3d11.samplerLodBias to lower texture detail on distant objects, saving critical memory bandwidth on mobile chipsets.
* Synchronous Relief: Uses relaxedBarriers to prevent GPU "stalling" and improves frame pacing.
Hardware Compatibility: Includes specific legacy boosters for D3D9 and D3D11 titles to ensure stability across different game engines.


## Installation (Star / Winlator)
* Placement: Place the desired dxvk.conf file in the same directory as your game's executable (.exe) or anyfolder within your device storage, but the Download folder is recommended. 
* Container Setup: Open your Emulator/Container settings and navigate to the ENVIRONMENT VARIABLES tab.
Link the Config: Add a new variable named DXVK_CONFIG_FILE. Set the value to the direct path of your file (e.g., D:/ADM/dxvk.conf).

## Verification:
Launch your game and check the logs; a successful setup will show "Found config file" and list your "Effective configuration".


## Configuration Meanings Explained
* starengine.enabled: Activates the custom optimization logic within the Star Engine fork.
* starengine.drawThreshold: The trigger point (e.g., 800) where the engine begins skipping non-essential calls to maintain FPS.
* starengine.bindSkip: Forces the engine to skip a specific number of GPU binds; higher values (e.g., 4) maximize FPS in complex scenes.
* d3d11.samplerLodBias: Adjusts Level of Detail; a higher value (e.g., 3.5) simplifies distant textures to reduce GPU load.
* dxvk.maxChunkSize: Defines memory allocation size; set to 64 for balanced performance on 4GB-6GB RAM devices.
* dxgi.maxFrameLatency: Controls how many frames the CPU can prep ahead; use 2 to reduce input lag and prevent "pile-up" stutters.
* dxvk.enableDepthPrepass: Disables redundant depth checks; recommended as False for mobile Tile-Based GPUs.
* d3d9.deferSurfaceCreation: Ensures stability and faster boot times for older DirectX 9 titles.
* dxvk.tileCaching: Optimizes rendering specifically for mobile "tile-based" GPU architectures like Adreno.


## NOTE
* You can tweak your dxvk.conf to better suit your specific game having heavy stutter and lags which help in reducing its issue, but remember to always have a copy of your previous tweaked dxvk.conf file incase you want to fallback to it
* The XTREME config is best for low amd low-mid budget ADRENO GPU devices and as well may help in mid-high ADRENO GPU device.
* Sometimes the XTREME configure can break and cause game ro lose some UI groahics and also reduce graphics to the lowest.
* Fallback to light config if XTREME configuration caused black screen, jitters, missing UI elements and freezing or crashing in ganes

## License
This project is released under the MIT License. Permission is hereby granted to use, copy, and modify these configurations. Credit to the Star Emulator Community, jacojay, and Pissblaster for the underlying engine and wrapper developments.

> ADDITIONAL SETTINGS ADDED BY ISYGOLD, 
BASE DEVELOPER: @doitsujin
