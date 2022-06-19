-this script for who want to build twrp/shrp/pbrp and they dont have a pc with good performance 

-So to run it you need to froke or reclone to your repo

-you need recovery tree for your custom recovery (please if you got any problem check your recovery tree)

-finally change details on .github/workflows/"custom recovery".yml

what you need to change:

*Manifest: depend of your android version, please if you use custom rom use latest android

*Device: your device codename

*DT_Link: recovery tree

*DT_target: device/"manufacturer"/"codename"

*Target: if you have recovery partition use recoveryimage if you have A/B slot or no recovery partition use bootimage

*Path: on last line change "codename" to your codename

thanks
