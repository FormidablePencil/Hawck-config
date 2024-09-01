kmonad would search for 2 packages in 2 different places so I created sym links there to where they really were in the system:
sudo ln -s /usr/bin/setxkbmap /run/current-system/sw/bin/setxkbmap
sudo ln -s /usr/bin/sleep /run/current-system/sw/bin/sleep
in kmonad config fike:
  input  (device-file "/dev/input/by-path/platform-i8042-serio-0-event-kbd")

Could have updated this line instead of creating those sym links:
"/run/current-system/sw/bin/sleep 1 && /run/current-system/sw/bin/setxkbmap -option compose:ralt")


