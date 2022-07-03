Finally i made a script to build (twrp/shrp/pbrp) using github actions

Steps:

1) reclone the repo

2) change data on .github/workflows/(recovery).yml
 * a) Manifest: use your manifest
 * b) device: codename i.e: sweet
 * c) dt_link: device tree link
 * d) dt_path: i.e: device/xiaomi/sweet
 * e) target: 
    - if you have recovery partition: use recoveryimage
    - if you dont have recoveryimage: use bootimage
    - if you have A/B and recovery partition: use recoveryimage
    - if you dont have recovery partition and you have A/B: use bootimage
 * f) ot: if your device tree have (i.e: omni_sweet.mk) use: omni
               if your device tree have (i.e: twrp_sweet.mk) use: twrp

3) for device tree: 
   a) twrp: use Twrpdtgen
   b) pbrp: use Twrpdtgen + go to boardConfig.mk and remove # on Board size ...
   c) shrp: check shrp website to add needed flags

4) if you get an error check your device tree first
   or : use #errortemplate for Twrp Building support group on telegram (twrp only).
   for other: check shrp/pbrp community

5) if your recovery partition smaller than builded recovery. 
   a) build a small kernel
   b) compress your kernel

thanks
