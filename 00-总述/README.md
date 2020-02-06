# Overview

### ACPI Rename and Patch

-Try to use as few or as few renames and patches as possible. For example: `HDAS rename HDEF`,` EC0 rename EC`, `SSDT-OC-XOSI`, etc. Especially for underlined `MethodObj` (such as _STA, _OSI, etc.) rename ** use with caution **. In general:
  -No operating system patches required. For components that are restricted by the system and cannot work normally, customize the patch according to the specific situation of ACPI. ** Use with caution ** Operating System Patches with special requirements for operating systems.
  
  -Some machines don't need to rename and patch using brightness shortcuts. Use "PS2 keyboard mapping @ OC-xlivans" to achieve the same effect.
  -At present, most machines need "0D6D Patch" to solve the problem of wake up in seconds.
  -For the battery part, if the data must be split, battery renaming and patching are essential.
  -Most Thinkpad machines need "PTSWAK Comprehensive Patch and Extended Patch" to solve the problem that the breathing light does not recover after waking up.
  -For machines with a sleep button [Little Moon], please refer to the "PNP0C0E Sleep Correction Method" for the system crash when this button is pressed.
-Solving some problems requires enabling or disabling certain devices. To enable or disable the device:
  -ACPI Binary Rename-This method is very effective for single systems. For multiple systems, the impact of the rename on other systems should be assessed. ** Use with caution **.
  -"Preset Variables Method"-may affect other components or other systems. ** Use with caution **.
  -Counterfeit Devices-This method is very reliable. **Recommended Use** .

### Important patches

-*** SSDT-RTC0 ***-located in Counterfeit Devices

  Some machines crash during startup due to the disabled RTC [PNP0B00]. Use *** SSDT-RTC0 *** to solve this problem.

-*** SSDT-EC ***-Located in "Counterfeit EC"

  For ** 10.15 + ** system [notebook], if the EC controller name is not `EC`, add *** SSDT-EC ***, otherwise the system crashes during the startup phase.

