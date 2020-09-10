# eon_boot_logo
[animation_logo]
1. download all bootanimation_25m.zip.*
2. unzip
3. copy bootanimation.zip file to eon /data
4. ssh to eon
5. mount -o rw,remount /system
6. mv /system/media/bootanimation.zip /system/media/bootanimation.zip.old (back up original)
7. mv /data/bootanimation.zip /system/media/bootanimation.zip
8. chmod 655 /system/media/bootanimation.zip

[splash_LePro3]
1. replace logo*.png
2. run CREATE_LOGO.bat
3. upload splash.img file to eon /data
4. ssh to eon
5. su
6. dd if=/data/splash.img of=/dev/block/bootdevice/by-name/splash

[splash_OP3T]
1. OP3TInject -i LOGO.bin -D
2. replace fhd_oppo_1080_1920_result.raw.png
3. OP3TInject -j fhd -i LOGO.bin
4. upload modified.logo.bin to eon /data
5. ssh to eon
6. su
7. dd if=/data/modified.logo.bin of=/dev/block/platform/soc/624000.ufshc/by-name/LOGO
